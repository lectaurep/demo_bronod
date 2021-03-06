# Training demonstration for LECTAUREP

Creating transcription models for documents written by Maître Bronod.

## Data

### Train set

- 90 images, manually transcribed by Marie-Françoise Limon-Bonnet.
- In [escriptorium.inria.fr/document/317/images/](https://escriptorium.inria.fr/document/317/images/), images 1 to 90, included.

### Test set

- 9 images, manually transcribed by Marie-Françoise Limon-Bonnet.
- In [escriptorium.inria.fr/document/317/images/](https://escriptorium.inria.fr/document/317/images/), images 91 to 99, included.

### Evaluation set

- 1 image, manually transcribed by Marie-Françoise Limon-Bonnet.
- In [escriptorium.inria.fr/document/317/images/](https://escriptorium.inria.fr/document/317/images/), images 100.

Evaluation with [KaMI](https://kami-app.herokuapp.com/)

## Training

Models were trained with kraken version 3.0b25

### Model trained from scratch (fs)

Training lasted for about 1h30.

Cmd:

```
$ ketos train -o demobronod_fs_nfd -f page -t trainset.list --device cuda:1 --augment --threads 64 -u NFD -s '[1,120,0,1 Cr3,13,32 Do0.1,2 Mp2,2 Cr3,13,32 Do0.1,2 Mp2,2 Cr3,9,64 Do0.1,2 Mp2,2 Cr3,9,64 Do0.1,2 S1(1x0)1,3 Lbx200 Do0.1,2 Lbx200 Do.1,2 Lbx200 Do]' -r 0.0001
```

Output:

```
[11.2333] Region eSc_dummyblock_ without coordinates 
[11.2929] Region eSc_dummyblock_ without coordinates 
[11.2956] Region eSc_dummyblock_ without coordinates 
[11.2983] Region eSc_dummyblock_ without coordinates 
[11.3014] Region eSc_dummyblock_ without coordinates 
[11.3031] Region eSc_dummyblock_ without coordinates 
[11.3061] Region eSc_dummyblock_ without coordinates 
[11.3087] Region eSc_dummyblock_ without coordinates 
[11.3104] Region eSc_dummyblock_ without coordinates 
[11.3132] Region eSc_dummyblock_ without coordinates 
[11.3154] Region eSc_dummyblock_ without coordinates 
[11.3192] Region eSc_dummyblock_ without coordinates 
[11.3228] Region eSc_dummyblock_ without coordinates 
[11.3264] Region eSc_dummyblock_ without coordinates 
[11.3293] Region eSc_dummyblock_ without coordinates 
[11.3328] Region eSc_dummyblock_ without coordinates 
[11.3350] Region eSc_dummyblock_ without coordinates 
[11.3387] Region eSc_dummyblock_ without coordinates 
[11.3410] Region eSc_dummyblock_ without coordinates 
[11.3437] Region eSc_dummyblock_ without coordinates 
[11.3454] Region eSc_dummyblock_ without coordinates 
[11.3482] Region eSc_dummyblock_ without coordinates 
[11.3510] Region eSc_dummyblock_ without coordinates 
[11.3540] Region eSc_dummyblock_ without coordinates 
[11.3565] Region eSc_dummyblock_ without coordinates 
[11.3588] Region eSc_dummyblock_ without coordinates 
[11.3616] Region eSc_dummyblock_ without coordinates 
[11.3652] Region eSc_dummyblock_ without coordinates 
[11.3682] Region eSc_dummyblock_ without coordinates 
[11.3717] Region eSc_dummyblock_ without coordinates 
[11.3745] Region eSc_dummyblock_ without coordinates 
[11.3763] Region eSc_dummyblock_ without coordinates 
[11.3782] Region eSc_dummyblock_ without coordinates 
[11.3802] Region eSc_dummyblock_ without coordinates 
[11.3828] Region eSc_dummyblock_ without coordinates 
[11.3842] Region eSc_dummyblock_ without coordinates 
[11.3868] Region eSc_dummyblock_ without coordinates 
[11.3891] Region eSc_dummyblock_ without coordinates 
[11.3907] Region eSc_dummyblock_ without coordinates 
[11.3917] Region eSc_dummyblock_ without coordinates 
[11.3944] Region eSc_dummyblock_ without coordinates 
[11.3977] Region eSc_dummyblock_ without coordinates 
[11.4002] Region eSc_dummyblock_ without coordinates 
[11.4024] Region eSc_dummyblock_ without coordinates 
[11.4049] Region eSc_dummyblock_ without coordinates 
[11.4074] Region eSc_dummyblock_ without coordinates 
[11.4095] Region eSc_dummyblock_ without coordinates 
[11.4117] Region eSc_dummyblock_ without coordinates 
[11.4142] Region eSc_dummyblock_ without coordinates 
[11.4156] Region eSc_dummyblock_ without coordinates 
[11.4184] Region eSc_dummyblock_ without coordinates 
[11.4205] Region eSc_dummyblock_ without coordinates 
[11.4233] Region eSc_dummyblock_ without coordinates 
[11.4256] Region eSc_dummyblock_ without coordinates 
[11.4291] Region eSc_dummyblock_ without coordinates 
[11.4327] Region eSc_dummyblock_ without coordinates 
[11.4363] Region eSc_dummyblock_ without coordinates 
[11.4385] Region eSc_dummyblock_ without coordinates 
[11.4415] Region eSc_dummyblock_ without coordinates 
[11.4441] Region eSc_dummyblock_ without coordinates 
[11.4466] Region eSc_dummyblock_ without coordinates 
[11.4502] Region eSc_dummyblock_ without coordinates 
[11.4527] Region eSc_dummyblock_ without coordinates 
[11.4532] Region eSc_dummyblock_ without coordinates 
[11.4558] Region eSc_dummyblock_ without coordinates 
[11.4587] Region eSc_dummyblock_ without coordinates 
[11.4616] Region eSc_dummyblock_ without coordinates 
[11.4651] Region eSc_dummyblock_ without coordinates 
[11.4669] Region eSc_dummyblock_ without coordinates 
[11.4697] Region eSc_dummyblock_ without coordinates 
[11.4721] Region eSc_dummyblock_ without coordinates 
[11.4744] Region eSc_dummyblock_ without coordinates 
[11.4763] Region eSc_dummyblock_ without coordinates 
[11.4789] Region eSc_dummyblock_ without coordinates 
[11.4814] Region eSc_dummyblock_ without coordinates 
[11.4849] Region eSc_dummyblock_ without coordinates 
[11.4865] Region eSc_dummyblock_ without coordinates 
[11.4894] Region eSc_dummyblock_ without coordinates 
[11.4920] Region eSc_dummyblock_ without coordinates 
[11.4947] Region eSc_dummyblock_ without coordinates 
[11.4976] Region eSc_dummyblock_ without coordinates 
[11.5005] Region eSc_dummyblock_ without coordinates 
[11.5041] Region eSc_dummyblock_ without coordinates 
[11.5069] Region eSc_dummyblock_ without coordinates 
[11.5096] Region eSc_dummyblock_ without coordinates 
[11.5122] Region eSc_dummyblock_ without coordinates 
[11.5147] Region eSc_dummyblock_ without coordinates 
[11.5176] Region eSc_dummyblock_ without coordinates 
[11.5206] Region eSc_dummyblock_ without coordinates 
[11.5232] Region eSc_dummyblock_ without coordinates 
Building training set  [#####-------------------------------]  507/3055
[12.5124] Text line is empty after transformations 
Building training set  [#################-------------------]  1475/3055  00:00:01
[13.6353] Text line is empty after transformations 
Building training set  [##################------------------]  1570/3055  00:00:01
[13.8444] Text line is empty after transformations 
Building training set  [#########################-----------]  2165/3055  00:00:01
[15.4021] Text line is empty after transformations 
Building training set  [##########################----------]  2285/3055  00:00:00
[15.7714] Text line is empty after transformations 
Building training set  [##################################--]  2895/3055  00:00:00
[17.9231] No boundary given for line 
Building training set  [####################################]  3055/3055          
Building validation set  [####################################]  352/352
[19.3515] alphabet mismatch: chars in training set only: {'_', '?', '-', ')', ':', '¨', '%', '&', 'X'} (not included in accuracy test during training) 
Initializing model ✓
stage 1/∞  [####################################]  3049/3049          Accuracy report (1) 0.0368 21096 20320
stage 2/∞  [####################################]  3049/3049          Accuracy report (2) 0.0424 21096 20201
stage 3/∞  [####################################]  3049/3049          Accuracy report (3) 0.1037 21096 18909
stage 4/∞  [####################################]  3049/3049          Accuracy report (4) 0.0979 21096 19031
stage 5/∞  [####################################]  3049/3049          Accuracy report (5) 0.1487 21096 17959
stage 6/∞  [####################################]  3049/3049          Accuracy report (6) 0.1742 21096 17421
stage 7/∞  [####################################]  3049/3049          Accuracy report (7) 0.1885 21096 17120
stage 8/∞  [####################################]  3049/3049          Accuracy report (8) 0.2481 21096 15862
stage 9/∞  [####################################]  3049/3049          Accuracy report (9) 0.2366 21096 16104
stage 10/∞  [####################################]  3049/3049          Accuracy report (10) 0.2347 21096 16144
stage 11/∞  [####################################]  3049/3049          Accuracy report (11) 0.2680 21096 15442
stage 12/∞  [####################################]  3049/3049          Accuracy report (12) 0.2878 21096 15025
stage 13/∞  [####################################]  3049/3049          Accuracy report (13) 0.2973 21096 14824
stage 14/∞  [####################################]  3049/3049          Accuracy report (14) 0.2843 21096 15098
stage 15/∞  [####################################]  3049/3049          Accuracy report (15) 0.2911 21096 14956
stage 16/∞  [####################################]  3049/3049          Accuracy report (16) 0.3084 21096 14589
stage 17/∞  [####################################]  3049/3049          Accuracy report (17) 0.3130 21096 14494

Moving best model demobronod_fs_nfd_12.mlmodel (0.287779673871824) to demobronod_fs_nfd_best.mlmodel
```

![image](https://user-images.githubusercontent.com/33317799/137226904-1465ad46-e0b2-4acc-986e-35f4dd2bd722.png)



### Model trained by finetuning generic_lectau_26.mlmodel (ft)

The initial model can be found here : [https://gitlab.inria.fr/dh-projects/kraken-models/master/transcription-models/generic_lectaurep_26.mlmodel](https://gitlab.inria.fr/dh-projects/kraken-models/-/raw/master/transcription%20models/generic_lectaurep_26.mlmodel)

Training also lasted for about 1h30.


Cmd: 
```
$ ketos train -o demobronod_ft_nfd --load generic_lectaurep_26.mlmodel --resize add -f page -t trainset.list --device cuda:0 --augment --threads 64 -u NFD -s '[1,120,0,1 Cr3,13,32 Do0.1,2 Mp2,2 Cr3,13,32 Do0.1,2 Mp2,2 Cr3,9,64 Do0.1,2 Mp2,2 Cr3,9,64 Do0.1,2 S1(1x0)1,3 Lbx200 Do0.1,2 Lbx200 Do.1,2 Lbx200 Do]' -r 0.0001
```

Output:
```
Loading existing model from generic_lectaurep_26.mlmodel ✓[2.7728] Region eSc_dummyblock_ without coordinates 
[2.7796] Region eSc_dummyblock_ without coordinates 
[2.7823] Region eSc_dummyblock_ without coordinates 
[2.7847] Region eSc_dummyblock_ without coordinates 
[2.7868] Region eSc_dummyblock_ without coordinates 
[2.7886] Region eSc_dummyblock_ without coordinates 
[2.7917] Region eSc_dummyblock_ without coordinates 
[2.7952] Region eSc_dummyblock_ without coordinates 
[2.7977] Region eSc_dummyblock_ without coordinates 
[2.7992] Region eSc_dummyblock_ without coordinates 
[2.8027] Region eSc_dummyblock_ without coordinates 
[2.8056] Region eSc_dummyblock_ without coordinates 
[2.8073] Region eSc_dummyblock_ without coordinates 
[2.8096] Region eSc_dummyblock_ without coordinates 
[2.8132] Region eSc_dummyblock_ without coordinates 
[2.8160] Region eSc_dummyblock_ without coordinates 
[2.8186] Region eSc_dummyblock_ without coordinates 
[2.8222] Region eSc_dummyblock_ without coordinates 
[2.8259] Region eSc_dummyblock_ without coordinates 
[2.8294] Region eSc_dummyblock_ without coordinates 
[2.8322] Region eSc_dummyblock_ without coordinates 
[2.8351] Region eSc_dummyblock_ without coordinates 
[2.8382] Region eSc_dummyblock_ without coordinates 
[2.8419] Region eSc_dummyblock_ without coordinates 
[2.8453] Region eSc_dummyblock_ without coordinates 
[2.8480] Region eSc_dummyblock_ without coordinates 
[2.8495] Region eSc_dummyblock_ without coordinates 
[2.8523] Region eSc_dummyblock_ without coordinates 
[2.8559] Region eSc_dummyblock_ without coordinates 
[2.8584] Region eSc_dummyblock_ without coordinates 
[2.8611] Region eSc_dummyblock_ without coordinates 
[2.8639] Region eSc_dummyblock_ without coordinates 
[2.8656] Region eSc_dummyblock_ without coordinates 
[2.8677] Region eSc_dummyblock_ without coordinates 
[2.8707] Region eSc_dummyblock_ without coordinates 
[2.8731] Region eSc_dummyblock_ without coordinates 
[2.8755] Region eSc_dummyblock_ without coordinates 
[2.8774] Region eSc_dummyblock_ without coordinates 
[2.8801] Region eSc_dummyblock_ without coordinates 
[2.8828] Region eSc_dummyblock_ without coordinates 
[2.8855] Region eSc_dummyblock_ without coordinates 
[2.8885] Region eSc_dummyblock_ without coordinates 
[2.8913] Region eSc_dummyblock_ without coordinates 
[2.8935] Region eSc_dummyblock_ without coordinates 
[2.8965] Region eSc_dummyblock_ without coordinates 
[2.8991] Region eSc_dummyblock_ without coordinates 
[2.9017] Region eSc_dummyblock_ without coordinates 
[2.9042] Region eSc_dummyblock_ without coordinates 
[2.9048] Region eSc_dummyblock_ without coordinates 
[2.9077] Region eSc_dummyblock_ without coordinates 
[2.9113] Region eSc_dummyblock_ without coordinates 
[2.9140] Region eSc_dummyblock_ without coordinates 
[2.9161] Region eSc_dummyblock_ without coordinates 
[2.9187] Region eSc_dummyblock_ without coordinates 
[2.9214] Region eSc_dummyblock_ without coordinates 
[2.9239] Region eSc_dummyblock_ without coordinates 
[2.9275] Region eSc_dummyblock_ without coordinates 
[2.9310] Region eSc_dummyblock_ without coordinates 
[2.9338] Region eSc_dummyblock_ without coordinates 
[2.9366] Region eSc_dummyblock_ without coordinates 
[2.9392] Region eSc_dummyblock_ without coordinates 
[2.9428] Region eSc_dummyblock_ without coordinates 
[2.9454] Region eSc_dummyblock_ without coordinates 
[2.9463] Region eSc_dummyblock_ without coordinates 
[2.9489] Region eSc_dummyblock_ without coordinates 
[2.9510] Region eSc_dummyblock_ without coordinates 
[2.9532] Region eSc_dummyblock_ without coordinates 
[2.9559] Region eSc_dummyblock_ without coordinates 
[2.9585] Region eSc_dummyblock_ without coordinates 
[2.9614] Region eSc_dummyblock_ without coordinates 
[2.9642] Region eSc_dummyblock_ without coordinates 
[2.9659] Region eSc_dummyblock_ without coordinates 
[2.9686] Region eSc_dummyblock_ without coordinates 
[2.9704] Region eSc_dummyblock_ without coordinates 
[2.9723] Region eSc_dummyblock_ without coordinates 
[2.9746] Region eSc_dummyblock_ without coordinates 
[2.9768] Region eSc_dummyblock_ without coordinates 
[2.9792] Region eSc_dummyblock_ without coordinates 
[2.9814] Region eSc_dummyblock_ without coordinates 
[2.9828] Region eSc_dummyblock_ without coordinates 
[2.9854] Region eSc_dummyblock_ without coordinates 
[2.9883] Region eSc_dummyblock_ without coordinates 
[2.9917] Region eSc_dummyblock_ without coordinates 
[2.9936] Region eSc_dummyblock_ without coordinates 
[2.9961] Region eSc_dummyblock_ without coordinates 
[2.9989] Region eSc_dummyblock_ without coordinates 
[3.0015] Region eSc_dummyblock_ without coordinates 
[3.0041] Region eSc_dummyblock_ without coordinates 
[3.0061] Region eSc_dummyblock_ without coordinates 
[3.0079] Region eSc_dummyblock_ without coordinates 
Building training set  [##----------------------------------]  178/3069
[3.5937] Text line is empty after transformations 
Building training set  [###---------------------------------]  268/3069
[3.6376] Text line is empty after transformations 
Building training set  [####--------------------------------]  344/3069
[3.6996] Text line is empty after transformations 
Building training set  [############################--------]  2460/3069  00:00:00
[7.1502] Text line is empty after transformations 
Building training set  [################################----]  2785/3069  00:00:00
[8.3704] No boundary given for line 
Building training set  [##################################--]  2900/3069  00:00:00
[8.8222] Text line is empty after transformations 
Building training set  [####################################]  3069/3069          
Building validation set  [####################################]  338/338
[10.2947] alphabet mismatch: chars in training set only: {'+', '%', '-', ':', 'X', '_', '&', ')'} (not included in accuracy test during training) 
[10.2948] alphabet mismatch: chars in validation set only: {'¨', '?'} (not trained) 
stage 1/∞  [####################################]  3063/3063          Accuracy report (1) 0.8503 19538 2924
stage 2/∞  [####################################]  3063/3063          Accuracy report (2) 0.9112 19538 1734
stage 3/∞  [####################################]  3063/3063          Accuracy report (3) 0.9245 19538 1475
stage 4/∞  [####################################]  3063/3063          Accuracy report (4) 0.9346 19538 1278
stage 5/∞  [####################################]  3063/3063          Accuracy report (5) 0.9376 19538 1219
stage 6/∞  [####################################]  3063/3063          Accuracy report (6) 0.9414 19538 1145
stage 7/∞  [####################################]  3063/3063          Accuracy report (7) 0.9464 19538 1047
stage 8/∞  [####################################]  3063/3063          Accuracy report (8) 0.9447 19538 1080
stage 9/∞  [####################################]  3063/3063          Accuracy report (9) 0.9531 19538 917
stage 10/∞  [####################################]  3063/3063          Accuracy report (10) 0.9529 19538 920
stage 11/∞  [####################################]  3063/3063          Accuracy report (11) 0.9551 19538 878
stage 12/∞  [####################################]  3063/3063          Accuracy report (12) 0.9561 19538 858
stage 13/∞  [####################################]  3063/3063          Accuracy report (13) 0.9588 19538 805
stage 14/∞  [####################################]  3063/3063          Accuracy report (14) 0.9581 19538 819
stage 15/∞  [####################################]  3063/3063          Accuracy report (15) 0.9586 19538 808
stage 16/∞  [####################################]  3063/3063          Accuracy report (16) 0.9611 19538 761
stage 17/∞  [####################################]  3063/3063          Accuracy report (17) 0.9601 19538 780
stage 18/∞  [####################################]  3063/3063          Accuracy report (18) 0.9608 19538 766
stage 19/∞  [####################################]  3063/3063          Accuracy report (19) 0.9607 19538 768
stage 20/∞  [####################################]  3063/3063          Accuracy report (20) 0.9574 19538 832
stage 21/∞  [####################################]  3063/3063          Accuracy report (21) 0.9624 19538 734

Moving best model demobronod_ft_nfd_16.mlmodel (0.9610502610297881) to demobronod_ft_nfd_best.mlmodel
```

![image](https://user-images.githubusercontent.com/33317799/137226790-a945e6e2-cdd8-4d39-a957-c6f3abf3f5c5.png)


## Evaluations

Best models are evaluated with `ketos test` in kraken version 3.0.5 (because `ketos test` failed to load images in version 3.0b25)

Resulting evaluations can be found in :

- MODEL FROM SCRATCH
	- [eval_demobronod_fs.txt](./eval_demobronod_fs.txt): evaluation of demobronod_fs_nfd_best.mlmodel
	- [eval_demobronod_fs_nonfd.txt](./eval_demobronod_fs_nonfd.txt): evaluation of demobronod_fs_nfd_best.mlmodel without implementing NFD normalization
- FINETUNED MODELS
	- [eval_demobronod_ft.txt](./eval_demobronod_ft.txt): evaluation of demobronod_ft_nfd_best.mlmodel
	- [eval_demobronod_ft_nonfd.txt](./eval_demobronod_ft_nonfd.txt):: evaluation of demobronod_ft_nfd_best.mlmodel without implementing NFD normalization

