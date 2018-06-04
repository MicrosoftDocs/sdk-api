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

# _CMSG_SIGNED_ENCODE_INFO structure


## -description


The <b>CMSG_SIGNED_ENCODE_INFO</b> structure contains information to be passed to 
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> if <i>dwMsgType</i> is CMSG_SIGNED.


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field cSigners

Number of elements in the <b>rgSigners</b> array.


### -field rgSigners

Array of pointers to 
			   <a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a>
				structures each holding signer information.


### -field cCertEncoded

Number of elements in the <b>rgCertEncoded</b> array.


### -field rgCertEncoded

Array of pointers to 
              <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_BLOB</a> 
				  structures, each containing an encoded certificate.


### -field cCrlEncoded

Number of elements in the <b>rgCrlEncoded</b> array.


### -field rgCrlEncoded

Array of pointers to 
                <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRL_BLOB</a> structures, each containing an encoded CRL.


### -field cAttrCertEncoded

Number of elements in the <b>rgAttrCertEncoded</b> array.
			 Used only if CMSG_SIGNED_ENCODE_INFO_HAS_CMS_FIELDS is defined. 


### -field rgAttrCertEncoded

Array of encoded attribute certificates. 
			 Used only if CMSG_SIGNED_ENCODE_INFO_HAS_CMS_FIELDS is defined. This array of encoded attribute certificates can be used with CMS for PKCS #7 processing.


## -see-also




<a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>
 

 

