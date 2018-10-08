---
UID: NS:wincrypt._CRYPT_ECC_CMS_SHARED_INFO
title: "_CRYPT_ECC_CMS_SHARED_INFO"
author: windows-sdk-content
description: Represents key-encryption key information when using Elliptic Curve Cryptography (ECC) in the Cryptographic Message Syntax (CMS) EnvelopedData content type.
old-location: security\crypt_ecc_cms_shared_info.htm
tech.root: seccrypto
ms.assetid: 858dbf61-5c4f-4bd6-b47c-0a1379119693
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PCRYPT_ECC_CMS_SHARED_INFO, CRYPT_ECC_CMS_SHARED_INFO, CRYPT_ECC_CMS_SHARED_INFO structure [Security], CRYPT_ECC_CMS_SHARED_INFO_SUPPPUBINFO_BYTE_LENGTH, PCRYPT_ECC_CMS_SHARED_INFO, PCRYPT_ECC_CMS_SHARED_INFO structure pointer [Security], _CRYPT_ECC_CMS_SHARED_INFO, security.crypt_ecc_cms_shared_info, wincrypt/CRYPT_ECC_CMS_SHARED_INFO, wincrypt/PCRYPT_ECC_CMS_SHARED_INFO"
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
 - CRYPT_ECC_CMS_SHARED_INFO
product: Windows
targetos: Windows
req.typenames: CRYPT_ECC_CMS_SHARED_INFO, *PCRYPT_ECC_CMS_SHARED_INFO
req.redist: 
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
 

 

