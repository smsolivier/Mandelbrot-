# Mandelbrot Calculator

This directory includes openMP and CUDA C++ implementations of the Mandelbrot Calculator

Example of code output (run with spokes deck) 
![alt text](https://github.com/smsolivier/Mandelbrot-/blob/master/spokes.png "Colored Mandelbrot Image")

Tested on Arch Linux with
* nvcc from CUDA toolkit 7.5
* gcc 6.1.1

Not tested on Windows or Macintosh 
	
Dependencies 
* gcc
* openMP
* CUDA (if run with CUDA enabled)
* EOG image viewer
* ffmpeg 
* python
* bash
* HDF5

## Running the code 
### openMP
./run deckname resolution or 

./run -omp deckname resolution
	
### CUDA
./run -cuda deckname resolution 
	
for help run ./run -h or ./run --help 

### Making a zoom movie 
./movie deckname moviename.mp4 

## Main Files:

### Mandelbrot.h 
header file that defines the Mandelbrot class and shared functions 
	
### run
python script that compiles and runs the programs

./run -h will show the help for using this program 
	
### movie
bash script that runs movie.cpp (from the Main directory)
	
run as ./movie deckname movieName 
	
settings for the movie are in the movie.cpp file in Main 

### map.ppm	
Portable Pixel Map image of the Mandelbrot Set generated by the code 

### mand.h5 
Image data stored in h5 format for use in other visualization software 

## Directories:
### Data:
storage location for data dumps
	
### Decks:
contains all the input decks

see current decks for the structure

Structure must match exactly 
		
### Functions:
helper functions such as progress bar and printing wall time 

### Main:
Contains the CUDA and openMP main files 
