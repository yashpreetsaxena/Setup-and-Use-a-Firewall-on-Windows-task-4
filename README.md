# Task 4: Setup and Use a Firewall on Windows

## Objective

The objective of this task was to configure and test basic firewall rules using Windows Defender Firewall to understand how network traffic can be filtered and controlled.

## Tool Used

* Windows Defender Firewall with Advanced Security
* Command Prompt

## System Information

* Operating System: Windows 11
* Firewall Tool: Windows Defender Firewall

## Steps Performed

### 1. Opened Windows Defender Firewall

Accessed Windows Defender Firewall with Advanced Security and reviewed existing inbound firewall rules.

### 2. Created a New Firewall Rule

A new inbound rule was created with the following configuration:

* Rule Type: Port
* Protocol: TCP
* Local Port: 23 (Telnet)
* Action: Block the Connection
* Profiles: Domain, Private, Public
* Rule Name: Block Telnet Port 23

### 3. Verified the Rule

Confirmed that the newly created firewall rule was enabled and configured to block incoming traffic on TCP port 23.

### 4. Tested the Configuration

Attempted to test the blocked port using:

```cmd
telnet localhost 23
```

The Telnet Client was not installed on the system, resulting in the following message:

```text
'telnet' is not recognized as an internal or external command,
operable program or batch file.
```

This confirmed that Telnet was unavailable on the system. The firewall rule itself was successfully created and verified through Windows Defender Firewall.

### 5. Removed the Test Rule

After verification and documentation, the test firewall rule was deleted to restore the original firewall configuration.

## Screenshots

The screenshots folder contains:

* Windows Defender Firewall main window
* Existing inbound rules
* Port rule configuration
* Block connection configuration
* Created firewall rule
* Command Prompt test result
* Firewall rule removal

## Key Concepts Learned

* Firewall Configuration
* Inbound and Outbound Rules
* Port Filtering
* Network Security
* Traffic Control
* Windows Defender Firewall Management

## Interview Questions

### What is a Firewall?

A firewall is a network security system that monitors and filters incoming and outgoing traffic based on predefined security rules.

### Difference Between Stateful and Stateless Firewalls?

* Stateful firewalls track active connections and make decisions based on connection state.
* Stateless firewalls inspect each packet independently.

### What are Inbound and Outbound Rules?

* Inbound rules control traffic entering the system.
* Outbound rules control traffic leaving the system.

### Why Block Port 23 (Telnet)?

Telnet sends data in plain text and is considered insecure. Blocking port 23 helps prevent unauthorized Telnet access.

### How Does a Firewall Improve Security?

A firewall protects systems by blocking unauthorized access, filtering malicious traffic, and enforcing network security policies.

## Conclusion

This task provided practical experience with Windows Defender Firewall. A custom rule was created to block inbound Telnet traffic on port 23, demonstrating how firewalls help secure systems by controlling network access and filtering traffic based on predefined rules.
