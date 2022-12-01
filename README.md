# Synthesized-CDMA2000-turboodor-Matlab

Design data
- RSC elbows designed with shift registers and modulo 2 adders, with v2 = 1101 = 15, v3 = 1111 = 17, reaction = 1011 = 13. poly2trellis(4, [13 15 17], 13)
- Viterbi decoding with block from Simulink library
 -Vibrate with block from Simulink library
- Turbo coder rate 1/5
- BPSK modulation and transmission on AWGN Channel.

Design stages:

1. Setting the default parameters for the Convolutional Encoder block in the library and checking the correctness of decoding without AWGN Channel. Data visualization input data, encoded data and decoded data.
2. Convolutional encoder design with shift registers and adders modulo 2, with imposed parameters. Input and data visualization data. Comparison with the coded data from item 1 to verify correctness of the designed encoder. 
3. Add decoder and check decoding correctness, without AWGN Channel. View input data, encoded data and decoded data. Comparison with the results of item 1.
4. Making turbo coder and turbo decoder. Check the correctness of decoding, without AWGN Channel. View input data, turbo coded data and turbo decoded data. 
5. Adding the necessary blocks for BPSK modulation / demodulation and block AWGN Channel block. Checks and views similar to 4.
6. Determination of the minimum SNR for which BER = 0, for running time to cover a minimum of 200 data bits. Calculation of gain for these conditions.
