# NFC Card Reader & Writer

Android and iOS NFC applications developed during my software engineering internship at Giantec Semiconductor in 2026. The applications use the phones' built-in NFC capabilities to read and write supported tags, display stored information, and record operation logs for testing and debugging.

This repository is a documentation-only portfolio of my contributions. Company source code, internal tools, and proprietary test data are not included.

## Project Overview

I worked with the software team on corresponding Android and iOS applications with the same core NFC workflow. The Android application was implemented in Java, and the iOS application used Swift, SwiftUI, and Core NFC.

My work covered mobile interface development, NFC data handling, physical-device testing, and debugging. Alongside the applications, I worked with chip design engineers to learn and reproduce an MCU-based hardware validation workflow, including RF waveform inspection and I²C protocol analysis.

## Core Features

- **Tag detection:** Detect supported nearby NFC tags and display tag technology information.
- **Read and write:** Read NDEF-formatted data and encode custom fields for writing to supported tags.
- **Operation logging:** Display detailed, timestamped operation information in a scrollable log, track the number of entries, and clear recorded logs.
- **Connection controls:** The Android interface provides a green control to connect to a tag and a red control to disconnect the active connection.
- **Interface feedback:** Display operation status and results to support testing and troubleshooting.

## Technology Stack

| Area | Technologies |
| --- | --- |
| Android | Java, Android SDK, Android Studio |
| iOS | Swift, SwiftUI, Core NFC |
| NFC data | NDEF, custom data encoding |
| Hardware validation | MCU-based test platform, oscilloscope, logic analyzer, RF, I²C |

## My Contributions

- Developed and tested corresponding Android and iOS NFC applications with the software team.
- Implemented NDEF reading and writing, custom data encoding, and timestamped operation logs.
- Designed mobile interfaces and debugged NFC workflows on physical devices.
- Used operation logs and status messages to investigate read/write issues and verify application responses.
- After training, independently reproduced an MCU-based test workflow and performed RF and I²C communication checks.

## Testing and Hardware Validation

### Physical-Device Testing

Tested the applications on physical Android and iOS devices to check tag detection, reading and writing, interface responses, and operation logging. This connected application behavior with actual NFC interactions rather than relying only on interface-level testing.

### RF Waveform Analysis

Used an oscilloscope to examine NFC RF waveforms within fixed bit-time intervals. I moved along the time axis and manually decoded bit values from carrier-pause timing to inspect the transmitted signal.

### I²C Protocol Analysis

Used a logic analyzer to inspect SDA/SCL timing, identify START/STOP conditions, and examine transmitted data and acknowledgment responses. This provided a separate view of communication on the MCU-based test platform.

## Engineering Takeaways

The project gave me practical experience implementing a similar workflow across two native mobile platforms and debugging software that interacts with physical hardware. It also helped me connect application logs with lower-level communication behavior, using different tools for mobile testing, RF inspection, and digital protocol analysis.

## Repository Scope

This README describes my internship work at a high level. It is not a runnable application or an official company release. Source code and internal development materials remain outside this public repository.
