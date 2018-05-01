---
UID: NS:wincrypt._CMSG_SIGNED_ENCODE_INFO
title: "_CMSG_SIGNED_ENCODE_INFO"
author: windows-driver-content
description: Contains information to be passed to CryptMsgOpenToEncode if dwMsgType is CMSG_SIGNED.
old-location: security\cmsg_signed_encode_info.htm
old-project: SecCrypto
ms.assetid: 93138744-8316-461b-908a-1eab47e83f63
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PCMSG_SIGNED_ENCODE_INFO, CMSG_SIGNED_ENCODE_INFO, CMSG_SIGNED_ENCODE_INFO structure [Security], _CMSG_SIGNED_ENCODE_INFO, _crypto2_cmsg_signed_encode_info, security.cmsg_signed_encode_info, wincrypt/CMSG_SIGNED_ENCODE_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CMSG_SIGNED_ENCODE_INFO, *PCMSG_SIGNED_ENCODE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CMSG_SIGNED_ENCODE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

