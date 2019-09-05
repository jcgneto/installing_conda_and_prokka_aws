# installing_conda_and_prokka_aws
Installation steps for conda and prokka on Amazon web services EC2

# Here are the steps I've taken (installation was done on Sept 5th of 2019)

1. Assuming your AWS EC2 instance is already created and functional (sudo apt update & sudo apt upgrade)
2. wget http://repo.continuum.io/archive/Anaconda3-2019.07-Linux-x86_64.sh
3. bash Anaconda3-2019.07-Linux-x86_64.sh
4. which python #check which python you are using and then probably do step 5 to move into home/ubuntu/anaconda3
5. source .bashrc
6. which python #again to check
7. test by running python and exit out of python
8. pwd to check your absolute path
9. install prokka ==  conda install -c bioconda prokka or
                       conda install -c bioconda/label/cf201901 prokka or
                       *this worked for me but you may want to use this instead
                       conda install -c conda-forge -c bioconda -c defaults prokka
10. check to see if prokka is working by running prokka, then prokka --version, then prokka --listdb
11. had to install cd-hit as well  conda install -c bioconda cd-hit 

Sources I have used to come up with this approach:

https://medium.com/@josemarcialportilla/getting-spark-python-and-jupyter-notebook-running-on-amazon-ec2-dec599e1c297

https://wszhan.github.io/2018/04/09/installing-anaconda-on-ec2.html

https://github.com/tseemann/prokka

https://repo.continuum.io/archive/

https://anaconda.org/bioconda/prokka

https://anaconda.org/bioconda/cd-hit
