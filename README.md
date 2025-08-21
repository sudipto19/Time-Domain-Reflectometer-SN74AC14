# Time Domain Reflectometer using SN74AC14

## Overview

This project implements a Time Domain Reflectometer (TDR) using the SN74AC14 hex inverting Schmitt trigger. A Time Domain Reflectometer is an electronic instrument used to characterize and locate faults in metallic cables (such as coaxial cables, twisted pair cables, and other transmission lines) by sending a signal pulse down the cable and analyzing the reflected signals.

## Key Features

- **Low-cost implementation** using readily available SN74AC14 IC
- **Cable fault detection** and localization
- **Impedance discontinuity measurement**
- **Open and short circuit detection**
- **Distance-to-fault calculation**

## How It Works

The TDR operates on the principle of time-domain reflectometry:

1. **Pulse Generation**: The SN74AC14 Schmitt trigger generates fast-rising edge pulses that are transmitted down the cable under test
2. **Reflection Analysis**: When the pulse encounters an impedance discontinuity (fault, connector, termination), part of the signal is reflected back
3. **Time Measurement**: The time difference between the transmitted pulse and received reflection is measured
4. **Distance Calculation**: Using the known velocity factor of the cable, the distance to the fault can be calculated from the time-of-flight measurements

## SN74AC14 Specifications

- **Function**: Hex Inverting Schmitt Trigger
- **Technology**: AC (Advanced CMOS)
- **Supply Voltage**: 2V to 6V
- **Propagation Delay**: ~4.5ns (typical)
- **Rise/Fall Time**: ~3ns (typical)
- **Input Hysteresis**: Provides noise immunity and clean switching

## Circuit Description

The circuit consists of:

- **Pulse Generator**: SN74AC14 configured as an oscillator/pulse generator
- **Transmission Path**: Connection to the cable under test
- **Reflection Detector**: Input circuitry to capture reflected signals
- **Timing Circuitry**: For measuring time-of-flight
- **Display/Output**: Interface for presenting results

## Applications

- **Cable Installation Testing**: Verify cable integrity during installation
- **Maintenance and Troubleshooting**: Locate faults in existing cable runs
- **Quality Assurance**: Test cable manufacturing quality
- **Network Infrastructure**: Ethernet and other data cable testing
- **RF/Coaxial Cable Testing**: Antenna feed lines and RF systems

## Technical Specifications

- **Frequency Range**: Depends on SN74AC14 switching characteristics
- **Cable Types**: Coaxial, twisted pair, single conductor
- **Measurement Range**: Limited by pulse rise time and timing resolution
- **Resolution**: Dependent on sampling rate and signal processing

## Circuit Images

### Prototype Board
![Circuit 1](Images/Circuit%201.jpeg)

### Schematic Diagram
![Schematic 1](Images/Schematic%201.jpg)

## Safety Considerations

- Ensure proper grounding
- Use appropriate voltage levels
- Disconnect power when making connections
- Follow standard electronics safety practices

## References

- SN74AC14 Datasheet (Texas Instruments)
- Time Domain Reflectometry principles
- Transmission line theory
- Cable testing standards

## License

This project is provided for educational and research purposes.

---

**Note**: This is an educational/prototype implementation. For commercial cable testing applications, consider professional TDR equipment with calibrated accuracy and compliance certifications.
