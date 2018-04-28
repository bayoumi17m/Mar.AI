# Mar.AI

1) The bizhawk emulator is required to run this project. Make sure to install the Bizhawk pre-reqs before installing the emulator.
2) Afterwards, in command prompt, run predict-server.py. 
3) After spinning up the tensorflow instance, run the bizhawk emulator and before loading the ROM. 
4) After loading the ROM, one can select a state and run play.py or simply run the demo.

## To Train

### Run the first run of the Search AI
Load a state and then load SearchAI.lua in order to generate a recording using the search AI. Recordings consist of a series of frames and a steering.txt file that contains the recorded steering values.

### Iterative Development Loop
I ran an iterative improvement loop that swaps between playing and generating new recordings. To bootstrap the process, you must first generate a recording using the search AI and create an initial weights file using train.py. Now start predict-server.py.

Now you can load a state and run PlayAndSearch.lua which alternates between playing and searching.

## References
TensorKart - The first MarioKart deep learning project, which we started from as our baseline.
Deep Learning for Real-Time Atari Game Play Using Offline Monte-Carlo Tree Search Planning - The idea for using a search-based AI for teaching the Convnet AI came from this paper.
A Reduction of Imitation Learning and Structured Prediction to No-Regret Online Learning - The DAGGER algorithm was first introduced in this paper.
MarioKart 64 NEAT - This AI uses the NEAT algorithm to genetically evolve a shallow neural network
weatherton/BizHawkMarioKart64 - Some MarioKart 64 scripts which we used as a reference for memory locations.
