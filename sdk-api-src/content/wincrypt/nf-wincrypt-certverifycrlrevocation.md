---
UID: NF:wincrypt.CertVerifyCRLRevocation
title: CertVerifyCRLRevocation function (wincrypt.h)
author: windows-sdk-content
description: Check a certificate revocation list (CRL) to determine whether a subject's certificate has or has not been revoked.
old-location: security\certverifycrlrevocation.htm
tech.root: SecCrypto
ms.assetid: a46ac5b5-bc44-4857-a7fb-4f35d438e3f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertVerifyCRLRevocation, CertVerifyCRLRevocation function [Security], _crypto2_certverifycrlrevocation, security.certverifycrlrevocation, wincrypt/CertVerifyCRLRevocation
ms.topic: function
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertVerifyCRLRevocation function


## -description


The <b>CertVerifyCRLRevocation</b> function check a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) to determine whether a subject's certificate has or has not been revoked. The new 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Certificate Chain Verification Functions</a> are recommended instead of the use of this function.


## -parameters




### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pCertId [in]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_info">CERT_INFO</a> structure of the certificate to be checked against the CRL.


### -param cCrlInfo [in]

Number of 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_crl_info">CRL_INFO</a> pointers in the <i>rgpCrlInfo</i> array.


### -param rgpCrlInfo [in]

Array of pointers to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_crl_info">CRL_INFO</a> structures.


## -returns



Returns <b>TRUE</b> if the certificate is not on the CRL and therefore is valid.
						

It returns <b>FALSE</b> if the certificate is on the list and therefore has been revoked and is not valid.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certverifycrltimevalidity">CertVerifyCRLTimeValidity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certverifytimevalidity">CertVerifyTimeValidity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certverifyvaliditynesting">CertVerifyValidityNesting</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>
 

 

