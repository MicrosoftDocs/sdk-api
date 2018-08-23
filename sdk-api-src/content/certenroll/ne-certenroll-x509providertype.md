---
UID: NE:certenroll.X509ProviderType
title: X509ProviderType
author: windows-sdk-content
description: Specifies the type of cryptographic provider.
old-location: security\x509providertype_enum.htm
old-project: seccertenroll
ms.assetid: 636ccb3a-ea66-4993-ac62-29409ce63eba
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: X509ProviderType, X509ProviderType enumeration [Security], XCN_PROV_DH_SCHANNEL, XCN_PROV_DSS, XCN_PROV_DSS_DH, XCN_PROV_EC_ECDSA_FULL, XCN_PROV_EC_ECDSA_SIG, XCN_PROV_EC_ECNRA_FULL, XCN_PROV_EC_ECNRA_SIG, XCN_PROV_FORTEZZA, XCN_PROV_INTEL_SEC, XCN_PROV_MS_EXCHANGE, XCN_PROV_NONE, XCN_PROV_REPLACE_OWF, XCN_PROV_RNG, XCN_PROV_RSA_AES, XCN_PROV_RSA_FULL, XCN_PROV_RSA_SCHANNEL, XCN_PROV_RSA_SIG, XCN_PROV_SPYRUS_LYNKS, XCN_PROV_SSL, certenroll/X509ProviderType, certenroll/XCN_PROV_DH_SCHANNEL, certenroll/XCN_PROV_DSS, certenroll/XCN_PROV_DSS_DH, certenroll/XCN_PROV_EC_ECDSA_FULL, certenroll/XCN_PROV_EC_ECDSA_SIG, certenroll/XCN_PROV_EC_ECNRA_FULL, certenroll/XCN_PROV_EC_ECNRA_SIG, certenroll/XCN_PROV_FORTEZZA, certenroll/XCN_PROV_INTEL_SEC, certenroll/XCN_PROV_MS_EXCHANGE, certenroll/XCN_PROV_NONE, certenroll/XCN_PROV_REPLACE_OWF, certenroll/XCN_PROV_RNG, certenroll/XCN_PROV_RSA_AES, certenroll/XCN_PROV_RSA_FULL, certenroll/XCN_PROV_RSA_SCHANNEL, certenroll/XCN_PROV_RSA_SIG, certenroll/XCN_PROV_SPYRUS_LYNKS, certenroll/XCN_PROV_SSL, security.x509providertype_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509ProviderType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509ProviderType
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509ProviderType enumeration


## -description


The <b>X509ProviderType</b> enumeration specifies the type of cryptographic provider. Providers implement cryptographic standards and algorithms in software and hardware. This enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> interfaces.


## -enum-fields




### -field XCN_PROV_NONE

No provider is identified.


### -field XCN_PROV_RSA_FULL

Supports the following algorithms:

<ul>
<li>Encryption: <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">RC2</a> and <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">RC4</a></li>
<li>Hashing: <a href="https://msdn.microsoft.com/en-us/library/ms721594(v=VS.85).aspx">MD5</a> and SHA</li>
<li>Key Exchange: <a href="https://msdn.microsoft.com/en-us/library/ms721604(v=VS.85).aspx">RSA</a></li>
<li>Signatures: RSA</li>
</ul>

### -field XCN_PROV_RSA_SIG

Supports the following algorithms:

<ul>
<li>Hashing: MD5 and SHA</li>
<li>Signatures: RSA</li>
</ul>

### -field XCN_PROV_DSS

Supports the following algorithms. This is a subset of the XCN_PROV_DSS_DH provider type.

<ul>
<li>Hashing: MD5 and SHA</li>
<li>Signatures: <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Digital Signature Standard</a> (DSS)</li>
</ul>

### -field XCN_PROV_FORTEZZA

Supports the Fortezza cryptographic card developed by NSA. This includes support for the following algorithms:

<ul>
<li>Encryption: Skipjack</li>
<li>Hashing: SHA</li>
<li>Key Exchange: KEA</li>
<li>Signatures: DSS</li>
</ul>

### -field XCN_PROV_MS_EXCHANGE

Supports cryptographic algorithms used by the Microsoft Exchange mail application and other applications compatible with Microsoft Mail.
This includes the following:

<ul>
<li>Encryption: <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">CAST</a></li>
<li>Hashing: MD5</li>
<li>Key Exchange: RSA</li>
<li>Signatures: RSA</li>
</ul>

### -field XCN_PROV_SSL

Supports the <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">Secure Sockets Layer protocol</a>. This includes the following algorithms:

<ul>
<li>Encryption: variable</li>
<li>Hashing: variable</li>
<li>Key Exchange: RSA</li>
<li>Signatures: RSA</li>
</ul>

### -field XCN_PROV_RSA_SCHANNEL

Supports RSA and <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">Schannel</a> protocols. This includes the following algorithms:

<ul>
<li>Encryption: RC4, <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Data Encryption Standard</a> (DES), 3DES</li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: RSA</li>
<li>Signatures: RSA</li>
</ul>

### -field XCN_PROV_DSS_DH

Supports the following algorithms:

<ul>
<li>Encryption: <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">CYLINK_MEK</a></li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Diffie-Hellman algorithm</a></li>
<li>Signatures: DSS</li>
</ul>

### -field XCN_PROV_EC_ECDSA_SIG

Microsoft currently does not provide a CSP of this type.


### -field XCN_PROV_EC_ECNRA_SIG

Microsoft currently does not provide a CSP of this type.


### -field XCN_PROV_EC_ECDSA_FULL

Microsoft currently does not provide a CSP of this type.


### -field XCN_PROV_EC_ECNRA_FULL

Microsoft currently does not provide a CSP of this type.


### -field XCN_PROV_DH_SCHANNEL

Supports the Diffie-Hellman and Schannel protocols. This includes the following algorithms:

<ul>
<li>Encryption: DES, 3DES</li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: Diffie-Hellman algorithm</li>
<li>Signatures: DSS</li>
</ul>

### -field XCN_PROV_SPYRUS_LYNKS

Microsoft currently does not provide a CSP of this type.


### -field XCN_PROV_RNG

Microsoft currently does not provide a CSP of this type.


### -field XCN_PROV_INTEL_SEC

Microsoft currently does not provide a CSP of this type.


### -field XCN_PROV_REPLACE_OWF

Microsoft currently does not provide a CSP of this type.


### -field XCN_PROV_RSA_AES

Supports the following algorithms:

<ul>
<li>Encryption: RC2, RC4, <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">AES</a></li>
<li>Hashing: MD5, SHA</li>
<li>Key Exchange: RSA</li>
<li>Signatures: RSA</li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 

