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

# _CRL_CONTEXT structure


## -description



			The <b>CRL_CONTEXT</b> structure contains both the encoded and decoded representations of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL). CRL contexts returned by any CryptoAPI function must be freed by calling the 
<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a> function.


## -struct-fields




### -field dwCertEncodingType

Type of encoding used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -field pbCrlEncoded

A pointer to the encoded CRL information.


### -field cbCrlEncoded

The size, in bytes, of the encoded CRL information.


### -field pCrlInfo

A pointer to 
<a href="https://msdn.microsoft.com/06a28de3-dd7c-4efe-9baa-20aac69d63f3">CRL_INFO</a> structure containing the CRL information.


### -field hCertStore

A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.


## -see-also




<a href="https://msdn.microsoft.com/06a28de3-dd7c-4efe-9baa-20aac69d63f3">CRL_INFO</a>



<a href="https://msdn.microsoft.com/1601d860-6054-4650-a033-ea088655b7e4">CRYPT_SIGN_MESSAGE_PARA</a>



<a href="https://msdn.microsoft.com/5dfa1c08-5d75-4ee4-bd65-ce56eb61ecce">CertAddCRLContextToStore</a>



<a href="https://msdn.microsoft.com/ec2361e6-a1e6-413a-828e-d543a09c88f8">CertAddEncodedCRLToStore</a>



<a href="https://msdn.microsoft.com/23d9dfb0-926d-443e-b960-a03338f1cc1b">CertCreateCRLContext</a>



<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>



<a href="https://msdn.microsoft.com/7bd21424-4f74-4bac-ab47-00d51ebdca1c">CertGetCRLFromStore</a>
 

 

