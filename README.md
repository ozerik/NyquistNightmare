# NyquistNightmare
Synthesizer signal mangler, uses a modulator/demodulator strategy

This is a signal processor whose primary design goal (but use it however you like!) was to degrade a signal as though it's being transmitted and received as a radio wave. It uses two VCOs that run as fast as 80MHz, far above human hearing. When tuned to certain frequencies, the two VCOs can pass a recognizable signal through them. This signal may contain very large amounts of low frequency content, and will certainly contain hifh frequency content, which need to be filtered out.

So there's two filters in the signal chain, first a simple high-pass to remove the rumble, then a standard resonant low-pass filter that can also be voltage controlled.

Finally, there's an auto-gain circuit in the signal path, which takes lower amplitude signals and amplifies them, and automatically attenuates higher amplitude signals so the output from the circuit won't go higher than the Eurorack standard of 10V peak to peak. This AGC is necessary since the NyquistNightmare can sound incredibly cool when it's very quiet, but then a tiny tweak to one of the knobs will send it screaming into harsh chaos territory.

The top four knobs of the PCB control the modulation and dmodulation of the signal. The left two knobs control the amplitude of the modulating signals used for the two VCOs. These have a very significant effect, the purity of a signal getting through will be much greater if the modulating signals are lower voltage, which seems counterintuitive to me. All four of those knobs interact in fascinating ways, and will probably be where most of the fun in this module will be had.

The three knobs below the square of knobs controls the filter. The left knob is the cutoff for the high-pass filter, with the counterclockwise position being fully open, and the clockwise position bein closed off. The middle knob controls the cutoff for the low-pass VCF, and the right knob controls the resonance of the low-pass VCF. The VCF will self-oscillate when the resonance is turned up past about 2 o'clock.

The bottom row of potentiometers control some levels. The left knob is a wet/dry control, with clockwise being fully wet, counterclockwise fully dry. The middle knob attenuates the CV coming in to control the low-pass VCF. The right knob is an effect volume knob that starts slipping into saturation/warm distortion past about 2 o'clock.

It's important to know that the effect volume knob only controls the volume of the *WET* effect. Because of the way the signal is processed, it can't turn down the dry signal.

The jacks: the left jack is audio input. The middle jack is the CV for the low-pass VCF. The right jack is the audio output.
