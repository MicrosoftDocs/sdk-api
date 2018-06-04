---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

