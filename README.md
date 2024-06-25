# SAPC: speech accessibility project competition
![photo1](https://github.com/XIUWEN-ZHENG/SAPC/assets/96778918/c7d5ac78-6096-4f97-86fd-1d2ab4a060bb)
Write something here

## Data Prepration
* To use the SAP data, sign our data user agreement [here](https://speechaccessibilityproject.beckman.illinois.edu/conduct-research-through-the-project).
* Download and rename the data folder into ```/DatasetDownload```, with the file structure as follows.

```plaintext
/DatasetDownload

 ### Audio Files ###
 ┣ SpeechAccessibility_{release}_000.7z
 ┣ SpeechAccessibility_{release}_001.7z
 ┣ ...
 ┣ SpeechAccessibility_{release}_011.7z

 ### Json Files I (per spk) ###
 ┣ SpeechAccessibility_{release}_Only_Json.7z

 ### Json Files II (overall) ###
 ┣ SpeechAccessibility_{release}_Split.json
 ┣ SpeechAccessibility_{release}_Split_by_Contributors.json
 ┣ SpeechAccessibility_{release}_Dimension_Category_Description.json

 ### Json Files III (mismatch check) ###
 ┣ SpeechAccessibility_{release}_Check_Brackets.json
 ┣ SpeechAccessibility_{release}_Check_Normalization.json
 ┣ SpeechAccessibility_{release}_Check_Abbreviations.json
 ┣ SpeechAccessibility_{release}_Check_WordErrorRate.json
```
* Build conda environment using ```bash steps/setup.sh```.
* Unzip the data package using ```bash steps/unzip.sh```, from ```/DatasetDownload``` into ```/data``` with the file structure as follows.
```plaintext
/data

### Raw Audio Files ###
┣ raw
┃ ┣ {spk_id_1}
┃ ┃ ┣ {spk_id_1}_{utt_id_1}_xxxx.wav
┃ ┃ ┣ {spk_id_1}_{utt_id_2}_xxxx.wav
┃ ┃ ┣ ...
┃ ┃ ┣ {spk_id_1}.json
┃ ┣ {spk_id_2}
┃ ┣ ...
### Json Files ###
┣ doc
┃ ┣ {spk_id_1}.json
┃ ┣ {spk_id_2}.json
┃ ┣ ...
┃
┃ ┣ SpeechAccessibility_{release}_Split.json
┃ ┣ SpeechAccessibility_{release}_Split_by_Contributors.json
┃ ┣ SpeechAccessibility_{release}_Dimension_Category_Description.json
┃
┃ ┣ SpeechAccessibility_{release}_Check_Brackets.json
┃ ┣ SpeechAccessibility_{release}_Check_Normalization.json
┃ ┣ SpeechAccessibility_{release}_Check_Abbreviations.json
┃ ┣ SpeechAccessibility_{release}_Check_WordErrorRate.json
```
* Preprocess the data using ```bash steps/preprocess.sh```.
