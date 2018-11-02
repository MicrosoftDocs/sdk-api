---
UID: NC:wincrypt.PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC
title: PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC
author: windows-sdk-content
description: Encrypts the private key and returns the encrypted contents in the pbEncryptedKey parameter.
old-location: security\pcrypt_encrypt_private_key_func.htm
tech.root: seccrypto
ms.assetid: aa6b8bca-4f0d-491e-ab38-5c273a01ca05
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC, PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC callback, PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC callback function [Security], security.pcrypt_encrypt_private_key_func, wincrypt/PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC callback function


## -description


<p class="CCE_Message">[The <b>PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC</b> function is available for use in  the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC</b> function encrypts the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> and returns
the encrypted contents in the <i>pbEncryptedKey</i> parameter.  It is a callback function identified in a <a href="https://msdn.microsoft.com/5a60c96e-907a-409e-921c-59055452463f">CRYPT_PKCS8_EXPORT_PARAMS</a> structure that creates a PKCS #8 <a href="https://msdn.microsoft.com/5e80d6d1-2e38-4a2d-90df-e6e4000cd626">CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</a> structure.  The function must be implemented by the developer to suit each application.


## -parameters




### -param *pAlgorithm [out]

A pointer to a <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure to receive the algorithm used to encrypt the PrivateKeyInfo ASN.1 type found in the PKCS #8 standard.


### -param *pClearTextPrivateKey [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">plaintext</a> private key to be encrypted.


### -param *pbEncryptedKey [out]

A pointer to a <b>BYTE</b> buffer to receive the encrypted <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key BLOB</a>. If this parameter is <b>NULL</b>, <i>pcbEncryptedKey</i> will return the size, in bytes, of memory needed to contain the encrypted key on a subsequent call to this function.


### -param *pcbEncryptedKey [in, out]

A pointer to a <b>DWORD</b>  variable that contains the size, in  bytes, of the <i>pbEncryptedKey</i> buffer. If pbEncryptedKey is  <b>NULL</b>, then <i>pcbEncryptedKey</i>  is
set to the size, in bytes,  required to encrypt the
key. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pVoidEncryptFunc [in]

An  <b>LPVOID</b> variable that contains data used for encryption, such as key, initialization vector, and password.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).


If the function fails, it returns zero (<b>FALSE</b>).




## -see-also




<a href="https://msdn.microsoft.com/5a60c96e-907a-409e-921c-59055452463f">CRYPT_PKCS8_EXPORT_PARAMS</a>



<a href="https://msdn.microsoft.com/f59fd46b-5430-4aa2-85ba-961b416dbaac">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a>
 

 

