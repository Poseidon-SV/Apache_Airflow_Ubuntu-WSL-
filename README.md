```
> python --version
Python 3.9.13
```
``` 
> python -m venv py_airflow_env
> py_airflow_env\Scripts\activate 
```
` (py_airflow_env) C:\Users\98svm\Desktop\Shubham Verma\AI-ML\Apache_Airflow> `

GOTO: https://github.com/apache/airflow#installing-from-pypi

Find:
 * Installing from PyPI

 ```
 > pip install 'apache-airflow==2.6.2' --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-2.6.2/constraints-3.8.txt"
```
Not Working?? Do this instead -
```
> pip install apache-airflow
```

```md
D:\My Computer (Shubham)\AI\Apache_Airflow>airflow
WARNING:root:OSError while attempting to symlink the latest log directory
Usage: airflow [-h] GROUP_OR_COMMAND ...

Positional Arguments:
  GROUP_OR_COMMAND

    Groups:
      celery         Celery components
      config         View configuration
      connections    Manage connections
      dags           Manage DAGs
      db             Database operations
      jobs           Manage jobs
      kubernetes     Tools to help run the KubernetesExecutor
      pools          Manage pools
      providers      Display providers
      roles          Manage roles
      tasks          Manage tasks
      users          Manage users
      variables      Manage variables

    Commands:
      cheat-sheet    Display cheat sheet
      dag-processor  Start a standalone Dag Processor instance
      info           Show information about current Airflow and environment  
      kerberos       Start a kerberos ticket renewer
      plugins        Dump information about loaded plugins
      rotate-fernet-key
                     Rotate encrypted connection credentials and variables   
      scheduler      Start a scheduler instance
      standalone     Run an all-in-one copy of Airflow
                     DAGs
      triggerer      Start a triggerer instance
      version        Show the version
      webserver      Start a Airflow webserver instance

Optional Arguments:
  -h, --help         show this help message and exit

airflow command error: the following arguments are required: GROUP_OR_COMMAND, see help above.
```

Install bash for easy tutorial follow:
```
> wsl --install -d Ubuntu 
```
```bash
Enter new UNIX username: shubham
17Shu6@irflow23ver
New password:
Retype new password:
passwd: password updated successfully
Installation successful!
Windows Subsystem for Linux is now available in the Microsoft Store!
You can upgrade by running 'wsl.exe --update' or by visiting https://aka.ms/wslstorepage
Installing WSL from the Microsoft Store will give you the latest WSL updates, faster.
For more information please visit https://aka.ms/wslstoreinfo

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

Welcome to Ubuntu 22.04.2 LTS (GNU/Linux 5.10.102.1-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This message is shown once a day. To disable it please create the
/home/shubham/.hushlogin file.
shubham@Verma:~$
```
activate bash
```
D:\My Computer (Shubham)\AI\Apache_Airflow>bash
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

shubham@Verma:/mnt/d/My Computer (Shubham)/AI/Apache_Airflow$ 
$ source py_airflow_env/Scripts/activate
```
CONTINUE...
```bash
$ export AIRFLOW_HOME=.
$ sudo apt update
$ sudo apt install python3-venv python3-pip
$ pip install apache-airflow
$ pip install 'apache-airflow==2.6.2' --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-2.6.2/constraints-3.8.txt"
$ export AIRFLOW_HOME=~/airflow
$ airflow db init
$ source py_airflow_env/Scripts/activate
```
Cut-paste:
```bash
$ nautilus /home/shubham/airflow/
$ cp -r /home/shubham/airflow/ /mnt/d/  (cp -r /path/to/directory /path/to/location/new-name)
```
Back to Airflow(Run):
```
airflow webserver -p 8080
$ airflow standalone
```


```
sudo mkdir download
sudo mkdir desktop
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
apt --fix-broken install
sudo apt-get install libgconf2-4 libnss3-1d libxss1
sudo apt-get install chromium-browser
```

## Very Very important
### Use: `http://localhost:8080/`

to run your airflow if it shows server not able to connect in `http://0.0.0.0:8080/`
