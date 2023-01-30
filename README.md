# OpenPraparat

OpenPraparat is a code that simulates an artificial life model presented in the paper titled "Artificial Life using a Book and Bookmarker." 

>__Artificial Life using a Book and Bookmarker__ [[arXiv](https://arxiv.org/abs/2210.12854)] <br>
>Reproduction, development, and individual interactions are essential topics in artificial life. The cellular automata, which can handle these in a composite way, is highly restricted in its form and behavior because it represents life as a pattern of cells. In contrast, the virtual creatures proposed by Karl Sims have a very high degree of freedom in terms of morphology and behavior. However, they have limited expressive capacity in terms of those viewpoints. This study carefully extracts the characteristics of the cellular automata and Sims models to propose a new artificial life model that can simulate reproduction, development, and individual interactions while exhibiting high expressive power for morphology and behavior. The simulation was performed by sequentially reading a book with genetic information and repeatedly executing four actions: expansion, connection, disconnection, and transition. The virtual creatures in the proposed model exhibit unique survival strategies and lifestyles and acquire interesting properties in reproduction, development, and individual interactions while having freedom in morphology and behavior.

## Install 

### On Ubuntu
Open the terminal, and install the necessary packages using the following commands:
```
sudo apt install libglu1-mesa-dev mesa-common-dev
sudo apt install libglfw3 libglfw3-dev
```

Compile OpenPraparat using the following commands:
```
git clone https://github.com/A5size/OpenPraparat
cd ./OpenPraparat/src

make all install
```

### On macOS
Open the terminal, and install the necessary packages using the following commands:
```
brew install glfw3
```

Compile OpenPraparat using the following commands:
```
git clone https://github.com/A5size/OpenPraparat
cd ./OpenPraparat/src

make all install
```

### On Windows
To compile OpenPraparat on Windows, you need to install MSYS2. 
The instructions for installing MSYS2 are omitted here.

Once you have installed MSYS2, launch the mingw64.exe in MSYS2 
and install the necessary packages using the following commands:
```
pacman -Sy
pacman -Su

pacman -S mingw-w64-x86_64-gcc
pacman -S make
pacman -S git
pacman -S mingw-w64-x86_64-pkg-config
pacman -S mingw-w64-x86_64-glfw
pacman -S mingw-w64-x86_64-gcc-fortran
pacman -S mingw-w64-x86_64-gcc-libgfortran
```

Open the command prompt as an administrator and set the path: 
```
setx /M PATH "%PATH%;path\where\you\installed\msys64\mingw64\bin"
```

Launch mingw64.exe and compile OpenPraparat using the following commands: 
```
git clone https://github.com/A5size/OpenPraparat
cd ./OpenPraparat/src

make all install
```


## Operation Guide

### praparat_gui
This program launches the GUI to visualize the simulation. To start, click the "Target Directory" button and select the working directory where the input files are located.

#### Keys
Here is a list of some of the keys and the corresponding operation they perform: 
>W: Move forward <br>
>A: Move left <br>
>S: Move backward <br>
>D: Move right <br> 
>Space: Move up <br> 
>F: Move down <br> 
>M: Start simulation <br>
>P: Stop simulation <br>
>H: Hide photon <br>
>C: Change the cell drawing style <br>
>K: Change viewpoint <br>
>R: Change the field drawing style <br>
>Y: Take a screenshot <br>
>V: Start recording (sequentially output images) <br>
>O: Switch between day and night mode <br>
>Q: Exit the program <br>

#### Mouse
Left-click to select cells, right-click and drag to move the viewpoint. 


## Examples
```
tar -zxvf examples.tar.gz 
tree examples
examples
├── 01dumbbell_shaped
│   └── 01normal
│       ├── cells_file
│       ├── field.d
│       ├── input
│       └── seed.ini
└── 02reticulated
    ├── 01normal
    │   ├── cells_file
    │   ├── field.d
    │   └── input
    └── 02fix
        ├── cells_file
        ├── field.d
        ├── fix.ini
        ├── fragment.ini
        ├── input
        └── seed.ini
```
