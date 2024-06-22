本项目改自[stanleylsx](https://github.com/stanleylsx)大佬的[entity_extractor_by_ner](https://github.com/stanleylsx/entity_extractor_by_ner.git)项目

欢迎访问我的博客获取帮助：[麻花与千层饼](https://042333.xyz/myproject/256.html)

# 前言

本项目适用于支持CUDA11及以上的显卡。因为tensorflow1.x最高支持CUDA10，RTX30系及以上显卡最低支持CUDA11，因此我将tensorflow的版本提升到了tensorflow2.x。经测试tensorflow-gpu的2.6.0版本较为稳定，故采用此版本。



# 克隆必要包

hugging face bert-base-chinese

```
https://huggingface.co/google-bert/bert-base-chinese
```

BERT_NER_Chinese_TF2.X

```
https://github.com/M-YoungBWeN/BERT_NER_Chinese_TF2.X
```



# 环境配置

```
tensorflow-gpu==2.6.0

python==3.8

numpy==0.19.5

pandas==1.3.5

transformers==4.6.1

tqdm==4.66.1

tensorflow-addons==0.15.0

```



# 模型参数配置

[README.md](https://github.com/stanleylsx/entity_extractor_by_ner/blob/master/README.md)



# 附录

pip软件包详情

```
Package                 Version
----------------------- -----------
absl-py                 0.15.0
astunparse              1.6.3
cachetools              5.3.3
certifi                 2024.6.2
charset-normalizer      3.3.2
clang                   5.0
click                   8.1.7
colorama                0.4.6
filelock                3.15.1
flatbuffers             1.12
gast                    0.4.0
google-auth             2.30.0
google-auth-oauthlib    1.0.0
google-pasta            0.2.0
grpcio                  1.64.1
h5py                    3.1.0
huggingface-hub         0.0.8
idna                    3.7
importlib_metadata      7.1.0
joblib                  1.4.2
keras                   2.6.0
Keras-Preprocessing     1.1.2
Markdown                3.6
MarkupSafe              2.1.5
numpy                   1.19.5
oauthlib                3.2.2
opt-einsum              3.3.0
packaging               24.1
pandas                  1.3.5
pip                     24.0
protobuf                3.19.6
pyasn1                  0.6.0
pyasn1_modules          0.4.0
python-dateutil         2.9.0.post0
pytz                    2024.1
regex                   2024.5.15
requests                2.32.3
requests-oauthlib       2.0.0
rsa                     4.9
sacremoses              0.1.1
setuptools              69.5.1
six                     1.15.0
tensorboard             2.14.0
tensorboard-data-server 0.7.2
tensorflow-addons       0.15.0
tensorflow-estimator    2.15.0
tensorflow-gpu          2.6.0
termcolor               1.1.0
tokenizers              0.10.3
tqdm                    4.66.1
transformers            4.6.1
typeguard               2.12.1
typing-extensions       3.7.4
urllib3                 2.2.1
Werkzeug                3.0.3
wheel                   0.43.0
wrapt                   1.12.1
zipp                    3.19.2
```

conda软件包详情

```
# Name                    Version                   Build  Channel
absl-py                   0.15.0                   pypi_0    pypi
astunparse                1.6.3                    pypi_0    pypi
ca-certificates           2024.3.11            haa95532_0    defaults
cachetools                5.3.3                    pypi_0    pypi
certifi                   2024.6.2                 pypi_0    pypi
charset-normalizer        3.3.2                    pypi_0    pypi
clang                     5.0                      pypi_0    pypi
click                     8.1.7                    pypi_0    pypi
colorama                  0.4.6                    pypi_0    pypi
filelock                  3.15.1                   pypi_0    pypi
flatbuffers               1.12                     pypi_0    pypi
gast                      0.4.0                    pypi_0    pypi
google-auth               2.30.0                   pypi_0    pypi
google-auth-oauthlib      1.0.0                    pypi_0    pypi
google-pasta              0.2.0                    pypi_0    pypi
grpcio                    1.64.1                   pypi_0    pypi
h5py                      3.1.0                    pypi_0    pypi
huggingface-hub           0.0.8                    pypi_0    pypi
idna                      3.7                      pypi_0    pypi
importlib-metadata        7.1.0                    pypi_0    pypi
joblib                    1.4.2                    pypi_0    pypi
keras                     2.6.0                    pypi_0    pypi
keras-preprocessing       1.1.2                    pypi_0    pypi
libffi                    3.4.4                hd77b12b_1    defaults
markdown                  3.6                      pypi_0    pypi
markupsafe                2.1.5                    pypi_0    pypi
numpy                     1.19.5                   pypi_0    pypi
oauthlib                  3.2.2                    pypi_0    pypi
openssl                   3.0.14               h827c3e9_0    defaults
opt-einsum                3.3.0                    pypi_0    pypi
packaging                 24.1                     pypi_0    pypi
pandas                    1.3.5                    pypi_0    pypi
pip                       24.0             py38haa95532_0    defaults
protobuf                  3.19.6                   pypi_0    pypi
pyasn1                    0.6.0                    pypi_0    pypi
pyasn1-modules            0.4.0                    pypi_0    pypi
python                    3.8.19               h1aa4202_0    defaults
python-dateutil           2.9.0.post0              pypi_0    pypi
pytz                      2024.1                   pypi_0    pypi
regex                     2024.5.15                pypi_0    pypi
requests                  2.32.3                   pypi_0    pypi
requests-oauthlib         2.0.0                    pypi_0    pypi
rsa                       4.9                      pypi_0    pypi
sacremoses                0.1.1                    pypi_0    pypi
setuptools                69.5.1           py38haa95532_0    defaults
six                       1.15.0                   pypi_0    pypi
sqlite                    3.45.3               h2bbff1b_0    defaults
tensorboard               2.14.0                   pypi_0    pypi
tensorboard-data-server   0.7.2                    pypi_0    pypi
tensorflow-addons         0.15.0                   pypi_0    pypi
tensorflow-estimator      2.15.0                   pypi_0    pypi
tensorflow-gpu            2.6.0                    pypi_0    pypi
termcolor                 1.1.0                    pypi_0    pypi
tokenizers                0.10.3                   pypi_0    pypi
tqdm                      4.66.1                   pypi_0    pypi
transformers              4.6.1                    pypi_0    pypi
typeguard                 2.12.1                   pypi_0    pypi
typing-extensions         3.7.4                    pypi_0    pypi
urllib3                   2.2.1                    pypi_0    pypi
vc                        14.2                 h2eaa2aa_1    defaults
vs2015_runtime            14.29.30133          h43f2093_3    defaults
werkzeug                  3.0.3                    pypi_0    pypi
wheel                     0.43.0           py38haa95532_0    defaults
wrapt                     1.12.1                   pypi_0    pypi
zipp                      3.19.2                   pypi_0    pypi
```

