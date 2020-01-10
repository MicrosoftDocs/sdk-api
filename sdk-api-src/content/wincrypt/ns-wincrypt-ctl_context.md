---
UID: NS:wincrypt._CTL_CONTEXT
title: CTL_CONTEXT (wincrypt.h)
description: The CTL_CONTEXT structure contains both the encoded and decoded representations of a CTL.
old-location: security\ctl_context.htm
tech.root: SecCrypto
ms.assetid: 780edddf-1b44-4292-9156-4dfd5100adb8
ms.date: 12/05/2018
ms.keywords: '*PCTL_CONTEXT, CTL_CONTEXT, CTL_CONTEXT structure [Security], PCCTL_CONTEXT, PCCTL_CONTEXT structure pointer [Security], PCTL_CONTEXT, PCTL_CONTEXT structure pointer [Security], _crypto2_ctl_context, security.ctl_context, wincrypt/CTL_CONTEXT, wincrypt/PCCTL_CONTEXT, wincrypt/PCTL_CONTEXT'
f1_keywords:
- wincrypt/CTL_CONTEXT
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wincrypt.h
api_name:
- CTL_CONTEXT
targetos: Windows
req.typenames: CTL_CONTEXT, *PCTL_CONTEXT
req.redist: 
ms.custom: 19H1
---

# CTL_CONTEXT structure


## -description


The <b>CTL_CONTEXT</b> structure contains both the encoded and decoded representations of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">CTL</a>. It also contains an opened <b>HCRYPTMSG</b> handle to the decoded, cryptographically signed message containing the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a> as its <a href="https://docs.microsoft.com/windows/desktop/SecGloss/i-gly">inner content</a>.

CryptoAPI 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">low-level message functions</a> can be used to extract additional signer information.

A <b>CTL_CONTEXT</b> returned by any CryptoAPI function must be freed by calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a> function.


## -struct-fields




### -field dwMsgAndCertEncodingType

Type of encoding used. It is always acceptable to specify both the certificate and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

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
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a> structure contain the CTL information.


### -field hCertStore

A handle to the certificate store.


### -field hCryptMsg

Open <b>HCRYPTMSG</b> handle to a decoded, cryptographic-signed message containing the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a> as its <a href="https://docs.microsoft.com/windows/desktop/SecGloss/i-gly">inner content</a>.


### -field pbCtlContent

The encoded <a href="https://docs.microsoft.com/windows/desktop/SecGloss/i-gly">inner content</a> of the signed message.


### -field cbCtlContent

Count, in bytes, of <b>pbCtlContent</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddctlcontexttostore">CertAddCTLContextToStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedctltostore">CertAddEncodedCTLToStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certcreatectlcontext">CertCreateCTLContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certenumctlsinstore">CertEnumCTLsInStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfindctlinstore">CertFindCTLInStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfindsubjectinctl">CertFindSubjectInCTL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetandverifysigner">CryptMsgGetAndVerifySigner</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgsignctl">CryptMsgSignCTL</a>
 

 

