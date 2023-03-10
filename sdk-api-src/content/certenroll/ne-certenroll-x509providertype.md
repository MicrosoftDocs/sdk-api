---
UID: NE:certenroll.X509ProviderType
title: X509ProviderType (certenroll.h)
description: Specifies the type of cryptographic provider.
helpviewer_keywords: ["X509ProviderType","X509ProviderType enumeration [Security]","XCN_PROV_DH_SCHANNEL","XCN_PROV_DSS","XCN_PROV_DSS_DH","XCN_PROV_EC_ECDSA_FULL","XCN_PROV_EC_ECDSA_SIG","XCN_PROV_EC_ECNRA_FULL","XCN_PROV_EC_ECNRA_SIG","XCN_PROV_FORTEZZA","XCN_PROV_INTEL_SEC","XCN_PROV_MS_EXCHANGE","XCN_PROV_NONE","XCN_PROV_REPLACE_OWF","XCN_PROV_RNG","XCN_PROV_RSA_AES","XCN_PROV_RSA_FULL","XCN_PROV_RSA_SCHANNEL","XCN_PROV_RSA_SIG","XCN_PROV_SPYRUS_LYNKS","XCN_PROV_SSL","certenroll/X509ProviderType","certenroll/XCN_PROV_DH_SCHANNEL","certenroll/XCN_PROV_DSS","certenroll/XCN_PROV_DSS_DH","certenroll/XCN_PROV_EC_ECDSA_FULL","certenroll/XCN_PROV_EC_ECDSA_SIG","certenroll/XCN_PROV_EC_ECNRA_FULL","certenroll/XCN_PROV_EC_ECNRA_SIG","certenroll/XCN_PROV_FORTEZZA","certenroll/XCN_PROV_INTEL_SEC","certenroll/XCN_PROV_MS_EXCHANGE","certenroll/XCN_PROV_NONE","certenroll/XCN_PROV_REPLACE_OWF","certenroll/XCN_PROV_RNG","certenroll/XCN_PROV_RSA_AES","certenroll/XCN_PROV_RSA_FULL","certenroll/XCN_PROV_RSA_SCHANNEL","certenroll/XCN_PROV_RSA_SIG","certenroll/XCN_PROV_SPYRUS_LYNKS","certenroll/XCN_PROV_SSL","security.x509providertype_enum"]
old-location: security\x509providertype_enum.htm
tech.root: security
ms.assetid: 636ccb3a-ea66-4993-ac62-29409ce63eba
ms.date: 12/05/2018
ms.keywords: X509ProviderType, X509ProviderType enumeration [Security], XCN_PROV_DH_SCHANNEL, XCN_PROV_DSS, XCN_PROV_DSS_DH, XCN_PROV_EC_ECDSA_FULL, XCN_PROV_EC_ECDSA_SIG, XCN_PROV_EC_ECNRA_FULL, XCN_PROV_EC_ECNRA_SIG, XCN_PROV_FORTEZZA, XCN_PROV_INTEL_SEC, XCN_PROV_MS_EXCHANGE, XCN_PROV_NONE, XCN_PROV_REPLACE_OWF, XCN_PROV_RNG, XCN_PROV_RSA_AES, XCN_PROV_RSA_FULL, XCN_PROV_RSA_SCHANNEL, XCN_PROV_RSA_SIG, XCN_PROV_SPYRUS_LYNKS, XCN_PROV_SSL, certenroll/X509ProviderType, certenroll/XCN_PROV_DH_SCHANNEL, certenroll/XCN_PROV_DSS, certenroll/XCN_PROV_DSS_DH, certenroll/XCN_PROV_EC_ECDSA_FULL, certenroll/XCN_PROV_EC_ECDSA_SIG, certenroll/XCN_PROV_EC_ECNRA_FULL, certenroll/XCN_PROV_EC_ECNRA_SIG, certenroll/XCN_PROV_FORTEZZA, certenroll/XCN_PROV_INTEL_SEC, certenroll/XCN_PROV_MS_EXCHANGE, certenroll/XCN_PROV_NONE, certenroll/XCN_PROV_REPLACE_OWF, certenroll/XCN_PROV_RNG, certenroll/XCN_PROV_RSA_AES, certenroll/XCN_PROV_RSA_FULL, certenroll/XCN_PROV_RSA_SCHANNEL, certenroll/XCN_PROV_RSA_SIG, certenroll/XCN_PROV_SPYRUS_LYNKS, certenroll/XCN_PROV_SSL, security.x509providertype_enum
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: X509ProviderType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509ProviderType
 - certenroll/X509ProviderType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509ProviderType
---

# X509ProviderType enumeration


## -description

The <b>X509ProviderType</b> enumeration specifies the type of cryptographic provider. Providers implement cryptographic standards and algorithms in software and hardware. This enumeration is used by the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> and <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> interfaces.

## -enum-fields

### -field XCN_PROV_NONE:0

No provider is identified.

### -field XCN_PROV_RSA_FULL:1

Supports the following algorithms:

<ul>
<li>Encryption: <a href="/windows/desktop/SecGloss/r-gly">RC2</a> and <a href="/windows/desktop/SecGloss/r-gly">RC4</a></li>
<li>Hashing: <a href="/windows/desktop/SecGloss/m-gly">MD5</a> and SHA</li>
<li>Key Exchange: <a href="/windows/desktop/SecGloss/r-gly">RSA</a></li>
<li>Signatures: RSA</li>
</ul>

### -field XCN_PROV_RSA_SIG:2

Supports the following algorithms:

<ul>
<li>Hashing: MD5 and SHA</li>
<li>Signatures: RSA</li>
</ul>

### -field XCN_PROV_DSS:3

Supports the following algorithms. This is a subset of the XCN_PROV_DSS_DH provider type.

<ul>
<li>Hashing: MD5 and SHA</li>
<li>Signatures: <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Standard</a> (DSS)</li>
</ul>

### -field XCN_PROV_FORTEZZA:4

Supports the Fortezza cryptographic card developed by NSA. This includes support for the following algorithms:

<ul>
<li>Encryption: Skipjack</li>
<li>Hashing: SHA</li>
<li>Key Exchange: KEA</li>
<li>Signatures: DSS</li>
</ul>

### -field XCN_PROV_MS_EXCHANGE:5

Supports cryptographic algorithms used by the Microsoft Exchange mail application and other applications compatible with Microsoft Mail.
This includes the following:

<ul>
<li>Encryption: <a href="/windows/desktop/SecGloss/c-gly">CAST</a></li>
<li>Hashing: MD5</li>
<li>Key Exchange: RSA</li>
<li>Signatures: RSA</li>
</ul>

### -field XCN_PROV_SSL:6

Supports the <a href="/windows/desktop/SecGloss/s-gly">Secure Sockets Layer protocol</a>. This includes the following algorithms:

<ul>
<li>Encryption: variable</li>
<li>Hashing: variable</li>
<li>Key Exchange: RSA</li>
<li>Signatures: RSA</li>
</ul>

### -field XCN_PROV_RSA_SCHANNEL:12

Supports RSA and <a href="/windows/desktop/SecGloss/s-gly">Schannel</a> protocols. This includes the following algorithms:

<ul>
<li>Encryption: RC4, <a href="/windows/desktop/SecGloss/d-gly">Data Encryption Standard</a> (DES), 3DES</li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: RSA</li>
<li>Signatures: RSA</li>
</ul>

### -field XCN_PROV_DSS_DH:13

Supports the following algorithms:

<ul>
<li>Encryption: <a href="/windows/desktop/SecGloss/c-gly">CYLINK_MEK</a></li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: <a href="/windows/desktop/SecGloss/d-gly">Diffie-Hellman algorithm</a></li>
<li>Signatures: DSS</li>
</ul>

### -field XCN_PROV_EC_ECDSA_SIG:14

Microsoft currently does not provide a CSP of this type.

### -field XCN_PROV_EC_ECNRA_SIG:15

Microsoft currently does not provide a CSP of this type.

### -field XCN_PROV_EC_ECDSA_FULL:16

Microsoft currently does not provide a CSP of this type.

### -field XCN_PROV_EC_ECNRA_FULL:17

Microsoft currently does not provide a CSP of this type.

### -field XCN_PROV_DH_SCHANNEL:18

Supports the Diffie-Hellman and Schannel protocols. This includes the following algorithms:

<ul>
<li>Encryption: DES, 3DES</li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: Diffie-Hellman algorithm</li>
<li>Signatures: DSS</li>
</ul>

### -field XCN_PROV_SPYRUS_LYNKS:20

Microsoft currently does not provide a CSP of this type.

### -field XCN_PROV_RNG:21

Microsoft currently does not provide a CSP of this type.

### -field XCN_PROV_INTEL_SEC:22

Microsoft currently does not provide a CSP of this type.

### -field XCN_PROV_REPLACE_OWF:23

Microsoft currently does not provide a CSP of this type.

### -field XCN_PROV_RSA_AES:24

Supports the following algorithms:

<ul>
<li>Encryption: RC2, RC4, <a href="/windows/desktop/SecGloss/a-gly">AES</a></li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: RSA</li>
<li>Signatures: RSA</li>
</ul>

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
