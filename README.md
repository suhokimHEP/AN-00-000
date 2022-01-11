AN-00-000 area:

#Basic checkout instructions(Example with Daniel's info):

#First fork to your namespace

git config --global user.name "Suho Kim"

git config --global user.email "suho.kim@cern.ch"

#failure to set the next option can lead to the message

#'Basic: Access denied'

#if you use KRB access (http)

git config --global http.emptyAuth true

git clone --recursive https://:@gitlab.cern.ch:8443/tdr/papers/XXX-YY-NNN.git

#May need to fork and download utils folder too


#To build run:

bash makenote.sh

#Note you can set an enviroment variable to direct the output. (example using unix)

 export TDR\_TMP\_DIR=~/Path/To/Output/

#To pull changes from Head
git pull ssh://git@gitlab.cern.ch:7999/tdr/notes/AN-00-000.git

#Warning: make sure you direct to an empty directory. Running the makenote command
and running in a non-empty directory may delete the contents
