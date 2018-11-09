---
UID: NS:wincrypt._CRYPT_ENCRYPTED_PRIVATE_KEY_INFO
title: "_CRYPT_ENCRYPTED_PRIVATE_KEY_INFO"
author: windows-sdk-content
description: Contains the information in a PKCS #8 EncryptedPrivateKeyInfo ASN.1 type found in the PKCS #8 standard.
old-location: security\crypt_encrypted_private_key_info.htm
tech.root: seccrypto
ms.assetid: 5e80d6d1-2e38-4a2d-90df-e6e4000cd626
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO, CRYPT_ENCRYPTED_PRIVATE_KEY_INFO, CRYPT_ENCRYPTED_PRIVATE_KEY_INFO structure [Security], PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO, PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO structure pointer [Security], _CRYPT_ENCRYPTED_PRIVATE_KEY_INFO, security.crypt_encrypted_private_key_info, wincrypt/CRYPT_ENCRYPTED_PRIVATE_KEY_INFO, wincrypt/PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO"
ms.prod: windows
ms.technology: windows-sdk
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
 - CRYPT_ENCRYPTED_PRIVATE_KEY_INFO
product: Windows
targetos: Windows
req.typenames: CRYPT_ENCRYPTED_PRIVATE_KEY_INFO, *PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO
req.redist: 
---

# _CRYPT_ENCRYPTED_PRIVATE_KEY_INFO structure


## -description


<p class="CCE_Message">[The <b>CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</b> structure contains the information in a PKCS #8
EncryptedPrivateKeyInfo ASN.1 type found in the PKCS #8 standard.


## -struct-fields




### -field EncryptionAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that indicates the algorithm used for encryption.


### -field EncryptedPrivateKey

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the encrypted private key data.


## -see-also




<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/82fee86a-8704-4f22-8f11-f89509c5a0aa">CryptExportPKCS8Ex</a>



<a href="https://msdn.microsoft.com/f59fd46b-5430-4aa2-85ba-961b416dbaac">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a>



<a href="https://msdn.microsoft.com/aa6b8bca-4f0d-491e-ab38-5c273a01ca05">PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC</a>
 

 

