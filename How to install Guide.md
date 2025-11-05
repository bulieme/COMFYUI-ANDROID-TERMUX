# COMFYUI-ANDROID-TERMUX
Hey guys and Gals I figured out how to use ComfyUi on Android with Termux!

Install ComfyUI on Termux (Android) + PRoot
This will guide you on installing ComfyUi on Termux (Android) + PRoot Distro. Make sure that you have a high-end phone to actually make this usable. On a phone with 8GB RAM, launch the webui alone take at least ~ 2 GB RAM, thus making it impossible to load any model and process further.

## 1. Prerequisites
Instal ubuntu, please referr to this link: [Click here](https://github.com/arbyanmukmin/ubuntu-termux)

## 2. Installing ComfyUI
Run below commands sequentially as root user in Ubuntu.

* Install Dependencies for ComfyUI
```bash
apt update && apt upgrade -y && apt-get install curl git gcc make build-essential python3 python3-dev python3-distutils python3-pip python3-venv python-is-python3 -y

apt-get install libgl1 libglib2.0-0 libsm6 libxrender1 libxext6 -y
```

* Clone the repository and go to the directory
```
git clone https://github.com/comfyanonymous/ComfyUI
cd ComfyUI
```

* Python Quick fix when running it inside Ubuntu
```
export ANDROID_DATA=anything 
```

* Install required Python packages
```
pip install -r requirements.txt 
```

* Launch the webui. It will take some time to complete first-time installation then everything should be fine
```
python main.py --cpu
```

* Go to the localhost url: `http://127.0.0.1:8188`

* To start ComfyUI when making a new termux session
```
cd ubuntu-in-termux && ./startubuntu.sh
cd ComfyUI && python main.py --cpu
```
