# Analyze a phishing Email
## Objectives
1. [Introduction](#introduction)
2. [Sample phishing email](#samplephishingemail)
3. [Sender's email address for spoofing](#sender'semailaddressforspoofing)
4. [Email headers for discrepancies](#emailheadersfordiscrepancies)
5. [Identify suspicious links or attachments](#IdentifysuspiciouslinksorattachmentsM)
6. [Look for urgent or threatening language in the email body](#Lookforurgentorthreateninglanguageintheemailbody)

## INTRODUCTION
The first thing you need to know about phishing scams is that it's not the same as hacking. Phishing scams are all about tricking people into giving up their personal information, like credit card numbers or online banking passwords, by masquerading as a trustworthy entity in an email or text message.

It's called "phishing" because the criminals are fishing for your sensitive data from behind a computer screen. It only takes one click on the wrong link for everything you care about-your cash, contacts, photos-to be gone forever! 

## 📌 Types of Email Phishing
### 1. Spear Phishing
- Spear phishing is a kind of phishing attack that targets one person (or company) in particular. Spear phishing is often used in ransomware attacks, where someone holding your files hostage sends you an email pretending to be from a reputable company like your internet service provider or antivirus software telling you that your computer is infected with malware. If you click on the link in the email it will take you to a fake website that looks legitimate so when you enter your email address and password to "scan" your computer, you just gave the criminal access to all of your accounts.
### 2.CEO fraud
  - CEO fraud is a kind of spear-phishing that targets specific people, usually by spoofing high-profile or wealthy individuals. The criminal sends you an email pretending to be from the CEO of your company and asking for money.
  -  For example, they might ask you to wire some money to a new bank account and then provide instructions on how to do so. People who are less familiar with the company might fall for this or if it's sent to you from someone who looks legitimate, like the real CEO.
### 3. Vishing Attacks
- Vishing is a kind of phishing that takes place over the phone. The criminal calls you and pretends to be from a company like your internet service provider, a bank, etc. They will try to trick you into giving up financial information or by directing you to visit a website where they can steal your login information.
### 4. Smishing Attacks
- SMiShing is a kind of phishing that takes place over text messages. The criminal sends you a text message pretending to be from a company like your bank asking for account information or they might send you links to websites where they can steal it. A lot of times the criminals will pretend to be with Google or Microsoft so it's even harder to discern whether or not the message is fake.

  ## Sample phishing email
  ![image](https://github.com/NATTOMR/Day-2-Analyze-a-Phishing-Email-Sample/blob/main/M-Tech-Phishing-Emails-1024x724.jpg)

  ## Identify suspicious links or attachments
   ![image](https://github.com/NATTOMR/Day-2-Analyze-a-Phishing-Email-Sample/blob/main/Anatomy-of-a-Phishing-Email.webp)

  ## Look for urgent or threatening language in the email body
### Phishing emails depend heavily on the manipulation of human emotions. In an attempt to avoid a practical response, phishing emails often use urgent or threatening language to make the target respond quickly. It's common for these emails to say there is a problem that must be resolved quickly to avoid consequences. Some examples of common language in phishing emails include:

- A claim that suspicious activity or login attempts have occurred on your account
- A request to confirm personal or financial information
- Include a link to make a payment for products or services that have supposedly already been received
- Claim there's a problem with account or payment information
- Include a fake order confirmation or invoice


## Tools: Email client or saved email file (text), free online header analyzer
 ### Analyze an email header( Google Admin Toolbox Messageheader)
 
- On your computer, open Gmail.
- Open the email that you want to analyze.
- Next to Reply , click More Moreand then Show original.
- In a new window, the full header shows.
- Click Copy to clipboard.
- Open Google Admin Toolbox Messageheader.
- In the box, paste your header.
- Click Analyze the header above.

  ![image](https://github.com/NATTOMR/Day-2-Analyze-a-Phishing-Email-Sample/blob/main/Screenshot%202025-09-25%20100140.png)

   ![image](https://github.com/NATTOMR/Day-2-Analyze-a-Phishing-Email-Sample/blob/main/Screenshot%202025-09-25%20095444.png)

  ## Deliverables: A report listing phishing indicators found

 ## 📄 Phishing Analysis Report

- Subject: INTERNSHIP OFFER LETTERS
- From: ELEVATE LABs <hr@elevate-labs.info>
- To: elevatelabshire@gmail.com (with BCC: nattochakma29@gmail.com)
- Date: Sat, 20 Sep 2025

## 1. Header Analysis

- Return-Path: <hr@elevate-labs.info>

- SPF: ✅ Pass (209.85.220.41 authorized to send for elevate-labs.info).

- DKIM: ✅ Pass (d=elevate-labs.info; s=google).

- DMARC: Implicit pass (alignment seems OK).

- Received chain: Message sent through Google’s mail infrastructure (mail-sor-f41.google.com), consistent with SPF pass.

- Message-ID: <CAP_w3LED-H5rPP_Kg6WAhn7dQ7OSHJWXabWNxgiMaD3jVikX7w@mail.gmail.com> — suspicious because the Message-ID is a Gmail domain, while sender domain is elevate-labs.info.



## 2. Body Content Indicators

- Urgent / enticing language: “CONGRATS !!!”, “Congratulations! You’ve been selected” → strong emotional lure.

- Suspicious instructions: Asks recipient to use free online PDF splitter tools → unusual and unsafe request (normal HR would provide a personalized file directly).

- Attachments: Includes cyber 9.pdf. Phishing/malware risk if PDF contains malicious content or asks for credentials.

- Unsubscribe link: https://multisend-unsubscribe.gmail.com/$placeholder → placeholder unsub link (non-functional), suspicious.

- Generic greeting: “Dear Intern” → no personalization, typical of mass phishing.

## 3. Indicators of Potential Phishing

-Generic greeting — not personalized.

- Excessive enthusiasm (“CONGRATS !!!”) — common in scams.

- Suspicious Message-ID mismatch — Gmail-based ID with a custom domain sender.

- Unusual request — asking user to split the PDF themselves.

- Attachment included — potential malware or credential-harvesting doc.

- Placeholder unsubscribe link — unprofessional and suspicious.

## 4. Risk Assessment

- Technical checks (SPF/DKIM/DMARC): Pass ✅

- Content red flags: Multiple ❌

- Overall verdict: ⚠️ Medium-to-High Risk (Potential Phishing)

- Even though SPF and DKIM pass (suggesting the domain elevate-labs.info is authorized to send), the content and formatting strongly resemble a phishing/mass scam campaign.

## 5. Recommended Actions

- Do NOT open the attached PDF unless sandboxed or scanned with antivirus.

- Verify the sender domain:

- Check if elevate-labs.info is a legitimate registered company domain.

- Look up WHOIS records — new or obscure domain = higher risk.

- Contact organization directly: If Elevate Labs is real, verify by official website/contact page — not by replying to this email.

- Report the email as phishing in Gmail.

- Preserve evidence: Save the full .eml with headers if escalation is needed.
  
