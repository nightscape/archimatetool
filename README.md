# Docker image for command line Archi

The Archimate Modeleing Tool can be found here : https://github.com/archimatetool/archi

The image allows to run Archi command line. It as the Collaboration Plugin.


## Version

 - Archi : `4.10.0`
 - Collaboration Plugin : `0.8.7`

## Usage

### Export the html model :

When using an archimate file :
```
docker run --rm -it -v $PWD/output:/output -v $PWD/my-model-directory:/model:ro archimatetool --html.createReport /output/report --loadModel /model/model.archimate
```

When using Collaboration plugin :
```
docker run --rm -it -v $PWD/output:/output -v $PWD/my-git-project:/model:ro archimatetool --html.createReport /output/report --modelrepository.loadModel /model/
```
