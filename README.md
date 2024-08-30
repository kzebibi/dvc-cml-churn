## `Churn Detection with use of CML & DVC Tools `
    * Using different approaches for solving imbalancing dataset.
    * Using different Algorithms also.
-------------------
### Note
> `cml-churn.yaml` file is attached to this directory. You can put it in `.github/workflows/cml-churn.yaml` as usual.
------------------------
## Git 
``` bash
git init
git add .
git commit -m "msg"
git branch -M main 
git config --global --list 
git remote add origin <<ssh link or http link>>
git push

git status
```


## DVC
``` bash
dvc init 
dvc add ./data/ ./models/
dvc remote add --default myremote gdrive://1cNPh0ESwP2RTpM7oE59cbpzVQMnd_705
dvc push
dvd status
```

## Steps
``` bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
git init 
dvc init
dvc add ./data/ ./models/
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/kzebibi/dvc-cml-churn.git
dvc remote add -f --default myremote gdrive://1cNPh0ESwP2RTpM7oE59cbpzVQMnd_705
dvc remote modify myremote gdrive_use_service_account true
dvc remote modify myremote gdrive_service_account_json_file_path client_secret_545800426601-9fhh831ssubgffhuptclri81eu2b3rjg.apps.googleusercontent.com.json

git push -u origin main
dvc push


git branch dev 
git switch dev 

```


## Get data
``` bash
dvc pull

```