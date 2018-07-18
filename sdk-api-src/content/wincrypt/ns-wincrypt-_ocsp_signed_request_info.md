---
UID: NS:wincrypt._OCSP_SIGNED_REQUEST_INFO
title: "_OCSP_SIGNED_REQUEST_INFO"
author: windows-sdk-content
description: Contains information for an online certificate status protocol (OCSP) request with optional signature information.
old-location: security\ocsp_signed_request_info.htm
old-project: seccrypto
ms.assetid: b3ff0843-77d8-4a9e-a3ba-97e9c398919a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*POCSP_SIGNED_REQUEST_INFO, OCSP_SIGNED_REQUEST_INFO, OCSP_SIGNED_REQUEST_INFO structure [Security], POCSP_SIGNED_REQUEST_INFO, POCSP_SIGNED_REQUEST_INFO structure pointer [Security], _OCSP_SIGNED_REQUEST_INFO, security.ocsp_signed_request_info, wincrypt/OCSP_SIGNED_REQUEST_INFO, wincrypt/POCSP_SIGNED_REQUEST_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
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
tech.root: 
req.typenames: OCSP_SIGNED_REQUEST_INFO, *POCSP_SIGNED_REQUEST_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - OCSP_SIGNED_REQUEST_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

