---
UID: NS:wincrypt._OCSP_BASIC_SIGNED_RESPONSE_INFO
title: OCSP_BASIC_SIGNED_RESPONSE_INFO
author: windows-sdk-content
description: Contains a basic online certificate status protocol (OCSP) response with a signature.
old-location: security\ocsp_basic_signed_response_info.htm
tech.root: seccrypto
ms.assetid: 4b88a946-030f-490a-b46a-c42507e1268d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*POCSP_BASIC_SIGNED_RESPONSE_INFO, OCSP_BASIC_SIGNED_RESPONSE_INFO, OCSP_BASIC_SIGNED_RESPONSE_INFO structure [Security], POCSP_BASIC_SIGNED_RESPONSE_INFO, POCSP_BASIC_SIGNED_RESPONSE_INFO structure pointer [Security], security.ocsp_basic_signed_response_info, wincrypt/OCSP_BASIC_SIGNED_RESPONSE_INFO, wincrypt/POCSP_BASIC_SIGNED_RESPONSE_INFO"
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
 - OCSP_BASIC_SIGNED_RESPONSE_INFO
product: Windows
targetos: Windows
req.typenames: OCSP_BASIC_SIGNED_RESPONSE_INFO, *POCSP_BASIC_SIGNED_RESPONSE_INFO
req.redist: 
---

# OCSP_BASIC_SIGNED_RESPONSE_INFO structure


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
 

 

