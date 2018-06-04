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

# _CRYPT_ECC_CMS_SHARED_INFO structure


## -description


The <b>CRYPT_ECC_CMS_SHARED_INFO</b> structure represents key-encryption key information when using Elliptic Curve Cryptography (ECC) in the Cryptographic Message Syntax (CMS) EnvelopedData content type. This structure is used in a key-exchange scenario for exchange of keys to encrypt and decrypt content.  A pointer to this structure can be used in the <i>pvStructInfo</i> parameter of <a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> or <a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a> and is specified by the constant <b>ECC_CMS_SHARED_INFO</b>. For more information, see <a href="https://msdn.microsoft.com/f969f2a5-fcbb-4711-8523-ba22952ae952">Constants for CryptEncodeObject and CryptDecodeObject</a>.


## -struct-fields




### -field Algorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the object identifier of the key-encryption algorithm used to wrap the content-encryption key.


### -field EntityUInfo

An optional member that contains additional user keying material as an octet string supplied by the sending agent.


### -field rgbSuppPubInfo

An array of four bytes that represent the length, in bits, of the key-encryption key. The byte array is in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a> order.


The following table contains the definition of the array dimension.





#### CRYPT_ECC_CMS_SHARED_INFO_SUPPPUBINFO_BYTE_LENGTH (4)


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=92228">RFC 3278</a>
 

 

