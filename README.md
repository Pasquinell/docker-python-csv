# Docker for runing data science projects 
Template for building a docker image.
This image is based on [this](https://towardsdatascience.com/beginners-guide-to-data-science-python-docker-3181fd321a5c) article. I have made small tweaks in order to load a csv and then save a new csv in the localhost. This changes include change de requierements.txt file, including pandas on it, and then modifying the code to load, change and save a csv. For building this container go to the folder that contain this repo and then type (you need to have docker installed):
```
docker build -t docker_python_csv .
```
Then you will have a docker image installed in your machine. If you want to check that image write:
```
docker images
```
For running that image you will need to write this command
```
docker run -v /path/to/your/folder:/path/to/the/workspace docker_python_csv
```
which in my case (and just for the sake of remembering it, is)
```
docker run -v /Users/pasqui/code/sandbox/docker-python-csv:/app docker_python_csv
```
After running this, you should see a new csv in your current folder. 
