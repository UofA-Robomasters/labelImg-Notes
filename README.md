# LabelImg Notes
Since the original installation instructions on [lebalImg](https://github.com/tzutalin/labelImg) repository might not work for brand new Mac, I wrote this additional note to guide you for setting up [lebalImg](https://github.com/tzutalin/labelImg) on a brand now Mac.

- **Author:** Chenrui Lei (chenrui@ualberta.ca)
- **Date:** July 5th, 2018

# Tools

First, we need to download and install the tools we need to using before we install labelImg. The tools we need are homebrew.

#### Xcode

You can install Xcode in iTune store. The reason we install Xcode is because it will install other useful tools along with it automatically.

#### Homebrew

Please follow the instructions on [homebrew's website](https://brew.sh/) to install it or just use the cammand below.

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### Git

Git is a tool for software version controlling. We need to use it for downloading the source code of labelImg. You should have Git installed already if you have installed the Xcode. Otherwise, you can use the follow command to install it (note: this command uses Homebrew).

```bash
brew update
brew install git
```

# Installation

Now, we got the tools that we need. We can download the source code and install the labelImg on our brand now Mac.

#### Step 1: Download the source code

To download the source code of labelImg, we can use the folloing command,

```bash
git clone https://github.com/tzutalin/labelImg.git
cd labelImg
```

#### Step 2: Install dependencies

There are 3 dependencies we need for the labelImg. They are python3, pyqt5, and lxml. We will use the following command to install them.

- python3
```bash
brew install python3
```

- pyqt5
```bash
pip3 install pyqt5
```

- lxml
```bash
pip3 install lxml
```

#### Step 3: Compile the program

Run the command below,

```bash
make qt5py3
```

If there is not errors, your compilation is successful.

#### Step 4: Try to run the program

```bash
python labelImg.py
```

If there is a graphic window pops up, that means your labelImg is good to use.

# References

- https://github.com/tzutalin/labelImg
- https://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/
