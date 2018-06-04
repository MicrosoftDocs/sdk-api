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

# _OCSP_SIGNED_REQUEST_INFO structure


## -description


The <b>OCSP_SIGNED_REQUEST_INFO</b> structure contains information for an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) request with optional signature information.


## -struct-fields




### -field ToBeSigned

A BLOB that has been encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) and that contains the OCSP request information.


### -field pOptionalSignatureInfo

A pointer to an <a href="https://msdn.microsoft.com/1489e2a4-36f3-4e8c-9b99-7c2e396b3814">OCSP_SIGNATURE_INFO</a> structure that contains optional signature information.


## -remarks



In an OCSP client application, this structure receives an encoded <a href="https://msdn.microsoft.com/ec939c3b-f155-45f2-b507-6c2e6069a868">OCSP_REQUEST_INFO</a> structure as its <b>ToBeSigned</b> member. Optionally, a signature  of the <b>ToBeSigned</b>  member is stored in the <b>pOptionalSignatureInfo</b> member.

On the receiving end, an OCSP responder application decodes the incoming request to populate an <b>OCSP_SIGNED_REQUEST_INFO</b> structure and subsequently decodes the <b>ToBeSigned</b> member to obtain an <a href="https://msdn.microsoft.com/ec939c3b-f155-45f2-b507-6c2e6069a868">OCSP_REQUEST_INFO</a> structure.

OCSP applications can encode or decode this structure by using <b>X509_ASN_ENCODING</b> or <b>PKCS_7_ASN_ENCODING</b>.




## -see-also




<a href="https://msdn.microsoft.com/f969f2a5-fcbb-4711-8523-ba22952ae952">Constants for CryptEncodeObject and CryptDecodeObject</a>



<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>



<a href="https://msdn.microsoft.com/bf1935f0-1ab0-4068-9ed5-8fbb2c286b8a">CryptDecodeObjectEx</a>



<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>



<a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a>



<a href="https://msdn.microsoft.com/ee138918-ed7c-4980-8b18-64004a0dd7df">CryptSignAndEncodeCertificate</a>



<a href="https://msdn.microsoft.com/1489e2a4-36f3-4e8c-9b99-7c2e396b3814">OCSP_SIGNATURE_INFO</a>
 

 

