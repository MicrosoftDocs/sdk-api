---
UID: NS:wincrypt._CTL_CONTEXT
title: "_CTL_CONTEXT"
author: windows-sdk-content
description: The CTL_CONTEXT structure contains both the encoded and decoded representations of a CTL.
old-location: security\ctl_context.htm
old-project: SecCrypto
ms.assetid: 780edddf-1b44-4292-9156-4dfd5100adb8
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*PCTL_CONTEXT, CTL_CONTEXT, CTL_CONTEXT structure [Security], PCCTL_CONTEXT, PCCTL_CONTEXT structure pointer [Security], PCTL_CONTEXT, PCTL_CONTEXT structure pointer [Security], _CTL_CONTEXT, _crypto2_ctl_context, security.ctl_context, wincrypt/CTL_CONTEXT, wincrypt/PCCTL_CONTEXT, wincrypt/PCTL_CONTEXT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CTL_CONTEXT, *PCTL_CONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CTL_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CTL_CONTEXT structure


## -description



			The <b>CTL_CONTEXT</b> structure contains both the encoded and decoded representations of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CTL</a>. It also contains an opened <b>HCRYPTMSG</b> handle to the decoded, cryptographically signed message containing the 
<a href="https://msdn.microsoft.com/83b015b5-a650-4a81-a9f0-c3e8a9805c81">CTL_INFO</a> as its <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">inner content</a>.

CryptoAPI 
<a href="cryptography_functions.htm">low-level message functions</a> can be used to extract additional signer information.

A <b>CTL_CONTEXT</b> returned by any CryptoAPI function must be freed by calling the 
<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a> function.


## -struct-fields




### -field dwMsgAndCertEncodingType

Type of encoding used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -field pbCtlEncoded

A pointer to the encoded CTL.


### -field cbCtlEncoded

The size, in bytes, of the encoded CTL.


### -field pCtlInfo

A pointer to 
<a href="https://msdn.microsoft.com/83b015b5-a650-4a81-a9f0-c3e8a9805c81">CTL_INFO</a> structure contain the CTL information.


### -field hCertStore

A handle to the certificate store.


### -field hCryptMsg

Open <b>HCRYPTMSG</b> handle to a decoded, cryptographic-signed message containing the <a href="https://msdn.microsoft.com/83b015b5-a650-4a81-a9f0-c3e8a9805c81">CTL_INFO</a> as its <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">inner content</a>.


### -field pbCtlContent

The encoded <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">inner content</a> of the signed message.


### -field cbCtlContent

Count, in bytes, of <b>pbCtlContent</b>.


## -see-also




<a href="https://msdn.microsoft.com/83b015b5-a650-4a81-a9f0-c3e8a9805c81">CTL_INFO</a>



<a href="https://msdn.microsoft.com/e8858f75-77a1-4c5f-a3e3-a645c5e0f053">CertAddCTLContextToStore</a>



<a href="https://msdn.microsoft.com/4239d43e-187d-4f40-99ae-6f914b7577ac">CertAddEncodedCTLToStore</a>



<a href="https://msdn.microsoft.com/172c59ee-9e06-4169-aaa7-2624e3fcf015">CertCreateCTLContext</a>



<a href="https://msdn.microsoft.com/dac9f91e-8ed4-43ce-8147-485c2ed7edd5">CertEnumCTLsInStore</a>



<a href="https://msdn.microsoft.com/e5ed3b22-e96f-4e7d-a20e-eebed0a84d3c">CertFindCTLInStore</a>



<a href="https://msdn.microsoft.com/e0c81531-e649-45bb-bafe-bced00c7b16a">CertFindSubjectInCTL</a>



<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>



<a href="https://msdn.microsoft.com/380c9cf3-27a2-4354-b1c8-97cec33f4e44">CryptMsgGetAndVerifySigner</a>



<a href="https://msdn.microsoft.com/85ae8ce3-d0a7-4fcb-beaa-ede09d30930e">CryptMsgSignCTL</a>
 

 

