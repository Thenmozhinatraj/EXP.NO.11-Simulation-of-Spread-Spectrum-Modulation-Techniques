# EXP.NO.11-Simulation-of-Spread-Spectrum-Modulation-Techniques

11.Simulation of Spread Spectrum Modulation Techniques

# AIM
To simulate and analyze spread spectrum modulation techniques using Python by generating original data, performing modulation/demodulation, and spreading the signal.

# SOFTWARE REQUIRED
->Python 3.x

->Libraries: NumPy, Matplotlib

# ALGORITHMS
1. Generate Original Data

   Generate a random sequence of binary data (0s and 1s).

2. Demodulation

   Perform simple cumulative sum to simulate basic demodulation behavior.

3. Spread Spectrum Technique

   Map 0 to -1 and 1 to +1.

   Multiply each symbol with a random sequence of {-1, +1} to spread the signal.

4. Plot the Signals

   Plot the Original Data.

   Plot the Demodulated Signal.

   Plot the Spread Signal.

# PROGRAM
import numpy as np
 
import matplotlib.pyplot as plt

np.random.seed(0) 							

original_data = np.random.randint(0, 2, 1000)  # Random 0s and 1s

demodulated_signal = np.cumsum(original_data)

spread_signal = 2 * original_data - 1  # Map 0 -> -1, 1 -> 1

spread_signal = spread_signal * np.random.choice([-1, 1], size=1000)

fig, axs = plt.subplots(3, 1, figsize=(12, 6))

axs[0].plot(original_data, color='blue')

axs[0].set_title('Original Data')

axs[1].plot(demodulated_signal, color='blue')

axs[1].set_title('Demodulated Signal')

axs[2].plot(spread_signal, color='blue')

axs[2].set_title('Spread Signal')

plt.tight_layout()

plt.show()

# OUTPUT
![image](https://github.com/user-attachments/assets/341208c9-baf3-479e-9b14-e547d92d1371)




 
# RESULT / CONCLUSIONS

1. Successfully simulated a simple spread spectrum modulation technique.


2. Observed the randomization effect on the original data through the spread signal.


3. Learned how spreading a signal increases its bandwidth and provides robustness against interference.

