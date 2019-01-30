# SerialReader

This C++ code opens COMPort, writes to it, can read from it, and records the output in a CSV file. The reason for the "testamount" variable was because for the testing being done, a robotic arm was being moved on a set path several hundred times, with measurements being taken at specific locations along the path. Testamount allows all measurements taken at one location to be in the same column in Excel, which is very helpful.

If you are trying to write to a different COMPort than COM10, replace COM10 in the "ComPortName" variable with whatever number port you are trying to write to. If you are using COM9 or lower, the backslashes are most likely not necessary, as they solve a problem C++ has with writing to ports greater than 9.

If you get an error while running it in Microsoft Visual Studio that talks about precompiled headers problem, go to Project, Properties (at the bottom), C/C++, Precompiled Headers, then change "Precompiled Header" to "Not Using Precompiled Headers"

It was designed to be used for a Mitutoyo Digimatic Indicator, but can work for any serial device that shares "r" as the read command. If the read command is different, then the "testval" variable should be changed.
