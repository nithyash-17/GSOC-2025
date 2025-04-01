# Quantum Computing and Variational Quantum Eigensolver (VQE)

## Question  
Please comment on quantum computing or quantum machine learning. You can also comment on one quantum algorithm or one quantum software you are familiar with.  
You can also suggest methods you think are good and you would like to work on.  

## Answer  
The algorithm that gets me the most excited about quantum computation and machine learning is the Variational Quantum Eigensolver (VQE). The VQE is the most fundamental quantum system that uses quantum computers to literally do quantum calculations. The scope provided by VQE is limitless, finding use in drug discovery, material science and any system using many body quantum mechanics. The only limitation to VQE is it's naive approach, scaling problem and noise, many of these factors being limited by just current computational resources. With the ever expanding network of quantum computers and better qubits, VQE will soon be a staple algorithm used in research and industry.  

The VQE algorithm is used primarily to solve and find the ground state of a quantum system. This can also be a many body quantum system. VQE is a hybrid algorithm which means to say it uses both classical and quantum computers to find its results. In particular, it uses a quantum estimator and a classical optimizer to reach the ground state.  

### Steps to VQE  
1. **Estimate a wavefunction**  
   Depending on the problem, we assume a trial wavefunction | ψ(θ) > where θ is a vector of n parameters that parametrize this circuit.  

2. **Create an ansatz**  
   The wavefunction is modeled by a parametrized quantum circuit called an ‘ansatz’. This circuit has parametrized rotation gates depending on the same parameters θ. The circuit ends with a measurement such that the sum of the measures model the Hamiltonian of the system H.  

3. **Make the measurements**  
   The Hamiltonian can be written in terms of these measurements via appropriate transformations. The measured value will hence be the energy of the quantum system with the set parameters θ.  

4. **Attach a classical optimizer**  
   Just feed the output of the quantum circuit to a good classical optimizer. Through the developments in machine learning and AI over the past few years, we have a set of very good optimizers and almost any of them can be used. The optimizer runs and provides a new set of parameters that can be fed into the quantum circuit.  

5. **Iterate until convergence**  
   We repeat steps 2, 3, and 4 with the updated parameters to soon enter a minimum of energy. This is, as we are aware, the ground state energy of the system, and hence we have solved our problem with such a simple approach.  

The biggest problem I face with VQE is the choice of ansatz and other hyperparameters like the number of qubits, design of the circuit, entanglement properties, etc. I would really like to learn more about how we can best choose a model for a given problem and how we can use VQE in the minimum resources we have right now.  
