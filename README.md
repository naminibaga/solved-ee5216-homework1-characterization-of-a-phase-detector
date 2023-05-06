Download Link: https://assignmentchef.com/product/solved-ee5216-homework1-characterization-of-a-phase-detector
<br>
<strong>Objective: Characterization of a Phase Detector </strong>

<ul>

 <li><strong>Experience to be Learnt from this Homework: </strong></li>

</ul>

To get familiar with the SPICE simulation for the characterization of a timing sensitive circuit and then convert the results into a behavior model. Such a model can be used to support more efficient system-level simulation using Verilog simulators.

<ul>

 <li><strong>Step-by-Step Procedure </strong></li>

</ul>

Consider the design and characterization process for a Phase Detector (PD) used to determine the polarity of the phase of two clock signal. The two 1GHz input clock signals are named <em>clk_ref</em> and <em>clk_target</em>. The output is an onebit flag signal, called <em>lead_lag</em>. At each clock cycle, if the rising edge of <em>clk_target</em> arrives earlier than that of <em>clk_ref</em>, then the output <em>lead_lag</em> becomes ‘0’ (to indicate a <em>leading condition</em>). On the other hand, if the rising edge of <em>clk_target</em> arrives later than that of <em>clk_ref</em>, then the output <em>lead_lag</em> becomes ‘1’ (to indicate a <em>lagging condition</em>).

<ul>

 <li>Compose the SPICE circuit files for each of the 3 PDs discussed in class – (1) simple Flip-Flop based PD, (2) A sense amplifier based PD, and (3) racing based PD with 2 Flip-Flops, 1 racing circuit, and 1 SR latch. (30%)</li>

 <li>Run pre-layout SPICE simulation with two scenarios in terms of the two clock signals – (1) <em>clk_target </em>lags <em>clk_ref </em>by 10ps, and (2) <em>clk_target </em>leads <em>clk_ref </em>by 10ps. Report your output waveforms, respectively for the 3 types of PDs. (10%)</li>

 <li>Run pre-layout SPICE simulation to characterize the “<strong>Flipping Input Phase (FIP)</strong>” using the “sweeping input stimuli” shown in Fig. 1 below. Note that the “<strong>Input Phase</strong>” here is defined as the “the phase of <em>clk_ref</em>” minus “the phase of <em>clk_target</em>”. Use a table to summarize the FIB values of the 3 different PDs. Note that, for a PD, a smaller absolute FIP value indicates a higher resolution. Rank the resolution of the 3 different PDs. (30%)</li>

</ul>

Input Phase -10ps -9ps                                   0ps                                  +9ps +10ps

(a) Sweeping Input stimuli to derive Flipping Input Phase (FIP) value

-4  -3  -2  -1   0   1    2    Input Phase (ps)

(b) The lead/lag signal of a PD (indicating a FIP value of -2ps)




Fig. 1. Illustration of the Flipping Input Phase (FIP) value of a PD.




1




<ul>

 <li>Try to compose the behavior model for each of the 3 PDs using Verilog while including the FIB values you have derived in (c). Also, develop a testbench in Verilog generating the above “sweeping input stimuli” to verify that your behavior models are correct in producing the expected FIP value for each of the 3 different PDs. (30%)</li>

</ul>