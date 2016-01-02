# Frequency Communication Thesis
*A set of frequencies to allow communication by air*

---

### Theory
A set of sound frequencies to transfer text data and hyperlinks. Using frequencies from 380 Hz to 3000 Hz with a space of 20 hz from each other, has a total of 131 slots of characters, 127 for standard ASCII table, and 4 for handshakes and frequency separator. 

### Frequency and wave type
Some recording devices are not able to collect high(> 3 MHz)/low(< 300 KHz) frequency well since they are not build for it. This project aims on mobile record devices which works better on **mid-high** ranges. The wave type chosen was **square** due its physical properties.

### Building the message
##### Handshake
The first segment of the message is a handshake, compound by 3 specific frequencies(380, 400, 420 Khz) + frequency separator (440 KHz):
380 + 440 + 400 + 440 + 420.

Once the handshake is interpreted by the listener, itself will be ready to convert the message into data.

##### Message
Starting by 460 KHz, with a **frequency separator of 20 KHz**, each frequency represents a content in the ASCII table. Example:  
The "abc" string:  
a -> 97th  
b -> 98th  
c -> 99th  
"a" turns into 2400 (460 + 97 * 20)  
Message in frequencies is:
 **"2400 + 440 + 2420 + 440 + 2440"**
 
### Tools
* http://onlinetonegenerator.com/ (for generating)
* https://play.google.com/store/apps/details?id=com.keuwl.audiofrequencycounter (for detection)

