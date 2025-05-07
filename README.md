# Process-Injection

The most popular covert launching technique.
As the name implies, malicious code is injected into another running process.
In the past, it was used to bypass AVs and host-based firewalls

How it’s done ?
PE Injection
The attacker process needs a handle to the target process.
Uses APIs like CreateToolhelp32Snapshot, Process32First, Process32Next, and OpenProcess.
Allocates memory in the target process and writes the malicious code into it.
Uses VirtualAllocEx and WriteProcessMemory.
Creates a remote thread to execute the injected code.
Uses CreateRemoteThread.

Demo:
![image](https://github.com/user-attachments/assets/de4a472a-21da-47d7-8abf-3bbba59af08f)
