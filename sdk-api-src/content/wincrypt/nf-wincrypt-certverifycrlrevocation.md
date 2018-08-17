---
UID: NF:wincrypt.CertVerifyCRLRevocation
title: CertVerifyCRLRevocation function
author: windows-sdk-content
description: Check a certificate revocation list (CRL) to determine whether a subject's certificate has or has not been revoked.
old-location: security\certverifycrlrevocation.htm
old-project: SecCrypto
ms.assetid: a46ac5b5-bc44-4857-a7fb-4f35d438e3f7
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CertVerifyCRLRevocation, CertVerifyCRLRevocation function [Security], _crypto2_certverifycrlrevocation, security.certverifycrlrevocation, wincrypt/CertVerifyCRLRevocation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertVerifyCRLRevocation
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertVerifyCRLRevocation function


## -description


The <b>CertVerifyCRLRevocation</b> function check a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) to determine whether a subject's certificate has or has not been revoked. The new 
<a href="cryptography_functions.htm">Certificate Chain Verification Functions</a> are recommended instead of the use of this function.


## -parameters




### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pCertId [in]

A pointer to the 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure of the certificate to be checked against the CRL.


### -param cCrlInfo [in]

Number of 
<a href="https://msdn.microsoft.com/06a28de3-dd7c-4efe-9baa-20aac69d63f3">CRL_INFO</a> pointers in the <i>rgpCrlInfo</i> array.


### -param rgpCrlInfo [in]

Array of pointers to <a href="https://msdn.microsoft.com/06a28de3-dd7c-4efe-9baa-20aac69d63f3">CRL_INFO</a> structures.


## -returns



Returns <b>TRUE</b> if the certificate is not on the CRL and therefore is valid.
						

It returns <b>FALSE</b> if the certificate is on the list and therefore has been revoked and is not valid.




## -see-also




<a href="https://msdn.microsoft.com/ff321fe8-df45-4a1d-b626-055fb0696438">CertVerifyCRLTimeValidity</a>



<a href="https://msdn.microsoft.com/9ccf9230-e998-4f82-9db0-6cbaa1c36850">CertVerifyTimeValidity</a>



<a href="https://msdn.microsoft.com/dc73a21d-5b55-45c4-80d2-220508d9f762">CertVerifyValidityNesting</a>



<a href="cryptography_functions.htm">Data Management Functions</a>
 

 

