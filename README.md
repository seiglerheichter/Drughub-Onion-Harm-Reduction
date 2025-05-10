# Safe Darkweb Access: A Harm Reduction Guide

---

## **1. Trust in Cryptography: TLS, CAs, and Asymmetric Encryption**

### **Why TLS and Certificate Authorities (CAs) Matter**
- **The Threat**: Attackers may impersonate legitimate sites (e.g., `torbrowser.org` → `t0rbrowser.net`) to trick users into downloading malware.
- **The Solution**:
  - **TLS (Transport Layer Security)** encrypts your connection and verifies website authenticity using certificates.
  - **Certificate Authorities (CAs)** act as trusted third parties to validate domain ownership.

#### **Verification Process**
When you visit `https://tails.boum.org`:
1. Your browser checks if the site’s TLS certificate:
   - Is **valid** (not expired/revoked).
   - Is **signed by a trusted CA** (e.g., Let’s Encrypt).
   - Matches the domain (`tails.boum.org`).
2. If any check fails, **do not proceed** – this indicates a potential phishing attack.

### **Asymmetric Encryption’s Role**
- **Key Pairs**:
  - **Public Key**: Shared openly (e.g., embedded in TLS certificates).
  - **Private Key**: Kept secret by the service (e.g., Tor Project’s server).
- **Proof of Ownership**:
  Servers use their private key to cryptographically prove they control the public key in their TLS certificate.

---

## **2. Open Source & Reputable Supply Chains**

### **Why Open Source is Critical**
- **Transparency**: Open-source code (e.g., Tor, Tails) allows:
  - Independent audits for backdoors/vulnerabilities.
  - Verification that compiled software matches the source code.
- **Example**:
  Tor Browser uses **reproducible builds** – developers can compile the code and confirm it matches the official download.

### **Supply Chain Risks**
- **Historical Attacks**:
  In 2016, attackers [compromised a Linux mirror](https://www.zdnet.com/article/linux-mint-website-hacked-to-serve-backdoored-iso/) to distribute malware.
- **Mitigation Strategies**:
  - **GPG Signatures**: Verify downloads using project-provided keys (e.g., [Tails’ instructions](https://tails.boum.org/install/expert/index.en.html)).
  - **HTTPS Only**: Download software exclusively from official sites over HTTPS.
  - **Avoid Third-Party Mirrors**: Even if faster, they pose tampering risks.

---

## **3. Asymmetric Encryption & .onion Addresses**

### **How .onion Addresses Work**
- **Key Derivation**:
  - A Tor onion service generates a public/private key pair.
  - The `.onion` address is a **hashed representation of the public key** (e.g., `yj5nzxm7d6shkb2i.onion`).
- **Cryptographic Proof**:
  The service uses its **private key** to prove ownership of the onion address during connection. No CAs required – trust is established via mathematics.

### **Why This Matters**
- **Tamper-Proof Design**:
  Changing one character in the onion address creates a completely different public key, making phishing harder than with traditional domains.
- **Decentralized Trust**:
  Unlike DNS, Tor doesn’t rely on centralized registrars. Control is cryptographic and decentralized.

---

## **4. Reliable Sources for Onion Addresses**

### **The Phishing Threat**
- **Fake Onions**:
  Attackers create lookalike addresses (e.g., `facebookcorewwwi.onion` vs. `faceb00kcorewwwi.onion`).
- **Poisoned Directories**:
  Unofficial "darkweb directories" often list malicious onions.

### **Verification Best Practices**
1. **Official Channels**:
   - Get onion addresses from the service’s **clearnet website** (e.g., ProtonMail lists its onion at `proton.me`).
   - Use **PGP-signed lists** from trusted entities (e.g., Tor Project’s blog).
2. **Reputable Tools**:
   - Use Tor Browser’s built-in DuckDuckGo onion service for searches.
   - Cross-reference with multiple sources (e.g., [Dark.fail](https://dark.fail) – verify via PGP).
3. **Software Integrity**:
   - A compromised Tor Browser (e.g., from a fake download) can bypass all safeguards.

---

## **Critical Recommendations**

- **Use Tor Browser or Tails**:
  Preconfigured for anonymity. Disable JavaScript unless absolutely necessary.
- **Verify PGP Signatures**:
  Confirm downloads using developer-provided keys (e.g., [Qubes OS instructions](https://www.qubes-os.org/security/verifying-signatures/)).
- **Practice OpSec**:
  - Assume all activity is monitored.
  - Use encrypted communication (e.g., PGP email via [Proton Mail’s onion](https://proton.me/support/tor)).
  - Never reuse passwords – use [KeePassXC](https://keepassxc.org/).

---

## **Onions I trust**

**Disclaimer:** *These links are provided for informational purposes only. We are not responsible for the content or security of these websites. Accessing these links may be illegal in your jurisdiction. Proceed with caution and at your own risk.*

*   **Elysium:** `c64xviojl7b4ricdo75pzfpxlpwd6xnqfcgkcj2uqd3ipao5v5bz7kqd.onion`
*   **Topshell NL:** `qf353xjiompd2rt3bqqdoh2tpes2dptxk7kdashssl55obgzuqdkpoad.onion`
*   **Dark Matter:** `darkmandsl7rgq4kxdk5v3pxpwn3qj2iz77mcxzggt2eefki2kzvu3ad.onion`
*   **Brians Club:** `briansi5d5yifg44gpdff7gainrp4hmowt245s2l24ab2jj7af642vid.onion`
*   **Simply Steroids:** `2xckczwiwsl6taoqjbmpd5veewwfh27v7n3yw6pq3qis6nnzgqfamjyd.onion`
*   **MarsMarket:** `marsh2ssxqizlzqod22t2soahnbxk63ql722ydrgxkox5ep5ba2zc3qd.onion`
*   **Prime:** `primeyqiu4ohrvktq2lushzyzaejvetu3pjvdeb4t5ml6mwlzj3rpwad.onion`
*   **ColumbiaConnection:** `6cgwnerkiykzpymf4lqabqd7xyva4msyiazlo3fhgip4brkjroz4sgid.onion`
*   **Anubis:** `anubiskjtaducsgs6wf55nixjadlhtdskimrl2vc4wm6gyp7pwjm77yd.onion`
*   **Dream V2:** `dreav2m66p4dntbw4r4ctsxpji3lsg3vwk5rvbi4kef47yipqwdktdqd.onion`
*   **Omega:** `omegac6qhrty6mcgwrcu7naha6yktulrcm3oqag457nkxcp4cvytskyd.onion`
*   **MGM Grand:** `2o6dshzzz65meuc4z2lzlqvmicijbuvyfr6ezobivohn7rr2me7xj2id.onion`
*   **SmokersCO:** `ap4swh6obar2kavix5bzlw5d2pnnnb4o3equdug62o2xkn5kjiajgqqd.onion`

---

**Disclaimer**: This guide is for educational purposes only. Accessing certain onion services may be illegal in your jurisdiction. Prioritize ethics and legality.
