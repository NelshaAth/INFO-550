# INFO-550 Data Science Toolkit Coursework

Hi! For assignment 3, I analyzed data files from two different air pollution samplers (units 91 and 96) to see if they were both fully functioning. 
To analyze the data you will need to have two R packages installed: tidyverse and lubridate. Both packages can be installed using R commands

```
installed_pkgs <- row.names(installed.packages())
pkgs <- c("tidyverse", "lubridate")
for(p in pkgs){
	if(!(p %in% install_pkgs)){
		install.packages(p)
	}
}
```

To run the script, from the project folder you can run:

```
Rscript -e "rmarkdown::render('Homework_3_Nelsha.Rmd')" 
```

This will create a file called Homework_3_Nelsha.html output in your directory, with the results.

## ASSIGNMENT 4
To download the Docker image of this project, pull the image:
```
docker pull nelshaath/info_550:latest
```
and then build the image
```
docker build -t info_550 .
```
Create a GUI to see output
```
docker run -e PASSWORD="SECRET123" -p 8787:8787 rocker/rstudio
```
and go to http://localhost:8787/ in your browser. 
	Username: rstudio
	Password: SECRET123
You will need to mount the directory to a local folder on your device. You must change the path to a folder on your device!!!
```
docker run -v /path/to/project/R:/info_550/Rmd -it info_550
```


