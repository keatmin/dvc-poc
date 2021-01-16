### DVC

#### Installation
```
python3 -m venv .venv
pip install dvc
git init
dvc init
```

#### Adding data

```
dvc add {data}
git add {data}.dvc
git commit -m "{message}"
git tag -a "v0.1" -m "Model v1.0, {n} data"
git push origin {branch}
git push origin {branch} {tagname}
```

#### Check out data
```
git checkout {tagname}
dvc checkout 
```

#### Keep code but change dataset
```
git checkout {tagname} data.dvc
dvc checkout data.dvc
```

#### Upload data
```
dvc remote add -d myremote s3://my-bucket/dvc-storage
dvc push
```

#### Download data
```
dvc pull
```
