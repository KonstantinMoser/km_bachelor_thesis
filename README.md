# Bachelor Thesis Konstantin Moser
This git repository contains the dataset and the written code of the Bachelor thesis: Intelligent and Behavioral-based Detection of Cyptominers in Resource-constrained Spectrum Sensors by Konstantin Moser

File List:<br />

Raspi_Dataset: Dataset Modeling the behaviour of the Raspberry Pi as a cvs file <br />
cryptojacker.txt: Altered version of the Linux.MulDrop.14 trojan as a shell script <br />
ML_Model_Creation: Jupyter Notebook to create the ML models <br /><br />

**Machine Learning Models**<br />
To create the models, all the code in *ML_Model_Creation.ipynb* has to be executed. Therefore, the Jupyter Notebook has to be started as a Google Collab Notebook. Insert the file into Google Drive, and Google Collab will automatically start upon executing the file.

**Cryptojacker**<br />
To install the cryptojacker and monitor the behaviour of the Raspberry Pi during infection, the ElectroSense Cyberspec image has to be installed beforehand. Then, connect to the device with the SSH port 22. The variable *TimeWindowSeconds* of the *new_sampler_50_rest.sh* script should be set to 5 seconds to measure the behaviour effectively.<br />

Afterwards, a timestamps.txt file has to be created, where the Unix timestamps will be
saved with the following command:
```
$ cat > timestamps.txt
```
Next, a new bash script has to created and opened with the *nano* command:
```
$ cat <<EOF > cryptojacker.sh
$ EOF
$ chmod +x cryptojacker.sh
$ nano cryptojacker.sh
```
Copy the contents of cryptojacker.txt into the *cryptojacker.sh* file and save it. Execute the malware by simply calling its name in the terminal:
```
$ ./cryptojacker.sh
```
Like this, the the cryptojacker is executed and should automatically run through the infection process.
