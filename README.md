# Shiny Demo App

A simple example showing how to deploy a [Shiny](https://shiny.rstudio.com/) app to cloud.gov.

## Usage

Get [access](https://cloud.gov/docs/getting-started/accounts/) to cloud.gov and [log in](https://cloud.gov/docs/getting-started/setup/).

Clone this repo, and change into the project directory. From there, push your app to cloud.gov.

```bash
~$ cf push
```

After a while of watching R modules compile, you'll see output similar to this:

```
Waiting for app to start...

name:              shiny-example
requested state:   started
routes:            shiny-example-comedic-numbat.app.cloud.gov
last uploaded:     Wed 13 May 16:54:09 EDT 2020
stack:             cflinuxfs3
buildpacks:        r

type:            web
instances:       1/1
memory usage:    256M
start command:   R -f app.R
     state     since                  cpu    memory        disk       details
#0   running   2020-05-13T20:54:29Z   0.0%   32K of 256M   8K of 1G
```

Visit the listed route in your web browser to see the application in action.

## Credits

Note - this demo app is taken from the collection provided [here](https://github.com/rstudio/shiny-examples).