# Data encryption using elgmal Elliptic Curve Cryptography

Elliptic curve cryptography (ECC) is a public-key cryptography system which is based on discrete logarithms structure of elliptic curves over finite fields. ECC is known for smaller key sizes, faster encryption, better security and more efficient implementations for the same security level as compared to other public cryptography systems (like RSA). ECC can be used for encryption (e.g. Elgamal), secure key exchange (ECC Diffie-Hellman) and also for authentication and verification of digital signatures.<br />

Elgamal Encryption and Decryption using Elliptic Curve Cryptography:<br />
• Suppose Alice wants to send to Bob an encrypted message. Both agree on a generator point ’G’.<br />
• Alice and Bob create public and private keys.<br />
• Alice<br />
private key = 𝑛𝑎<br />
public key = (𝑛𝑎)G<br />
• Bob<br />
private key = 𝑛𝑏<br />
public key = (𝑛𝑏)G<br />
• Alice takes plain text message ’M’ and encodes it onto a point 𝑃𝑚 from the elliptic group.<br />
• Alice chooses another random integer ’K’ from the interval [1,q-1].<br />
• The cipher text is a pair of points 𝐶𝑚= (KG, 𝑃𝑚 + K𝑃𝑏)<br />
• To decrypt bob computes the product of first point from 𝐶𝑚 and his private key 𝑛𝑏 (𝑛𝑏KG).<br />
• Bob then takes this product and subtracts it from the second point from 𝐶𝑚<br />
𝑃𝑚+ K𝑃𝑏 −𝑛𝑏(KG) = 𝑃𝑚 + K(𝑛𝑏G)− 𝑛𝑏 (KG) = 𝑃𝑚<br />
• Bob then decodes 𝑃𝑚 to get the message ’M’.<br />

Methodology:<br />
Message is mapped to a point in the elliptic curve and this is stored in a dictionary. The below diagram shows how each alphabet is mapped to a point in the dictionary<br />

implemenations are done in python
