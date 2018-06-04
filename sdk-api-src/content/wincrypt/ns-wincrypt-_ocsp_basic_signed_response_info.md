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

# _OCSP_BASIC_SIGNED_RESPONSE_INFO structure


## -description


 The <b>OCSP_BASIC_SIGNED_RESPONSE_INFO</b> structure contains a basic <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) response with a signature.


## -struct-fields




### -field ToBeSigned

A <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that has been encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) and that contains an encoded <a href="https://msdn.microsoft.com/f067bfa0-114b-4295-bbee-a963d8b64332">OCSP_BASIC_RESPONSE_INFO</a> structure.


### -field SignatureInfo

A pointer to signature information for the <b>ToBeSigned</b> data.


## -remarks



In an OCSP responder service, this structure receives an encoded <a href="https://msdn.microsoft.com/f067bfa0-114b-4295-bbee-a963d8b64332">OCSP_BASIC_RESPONSE_INFO</a> structure as its <b>ToBeSigned</b> member. The signature  of the <b>ToBeSigned</b>  member is stored in the <b>SignatureInfo</b> member. The encoded <b>OCSP_BASIC_SIGNED_RESPONSE_INFO</b> structure is stored in an <a href="https://msdn.microsoft.com/e3829739-dd10-4886-8048-cd1b1b712d56">OCSP_RESPONSE_INFO</a> structure.

On the receiving end, an OCSP client application must decode the <a href="https://msdn.microsoft.com/e3829739-dd10-4886-8048-cd1b1b712d56">OCSP_RESPONSE_INFO</a> <b>Value</b> member to obtain this structure and subsequently decode the <b>OCSP_BASIC_SIGNED_RESPONSE_INFO</b> <b>ToBeSigned</b> member to obtain an <a href="https://msdn.microsoft.com/f067bfa0-114b-4295-bbee-a963d8b64332">OCSP_BASIC_RESPONSE_INFO</a> structure.

OCSP applications can encode or decode this structure by using <b>X509_ASN_ENCODING</b> or <b>PKCS_7_ASN_ENCODING</b>.




## -see-also




<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a>



<a href="https://msdn.microsoft.com/1489e2a4-36f3-4e8c-9b99-7c2e396b3814">OCSP_SIGNATURE_INFO</a>
 

 

