---
UID: NC:wincrypt.PCRYPT_DECRYPT_PRIVATE_KEY_FUNC
title: PCRYPT_DECRYPT_PRIVATE_KEY_FUNC
author: windows-sdk-content
description: Decrypts the private key and returns the decrypted key in the pbClearTextKey parameter.
old-location: security\pcrypt_decrypt_private_key_func.htm
tech.root: seccrypto
ms.assetid: f59fd46b-5430-4aa2-85ba-961b416dbaac
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: PCRYPT_DECRYPT_PRIVATE_KEY_FUNC, PCRYPT_DECRYPT_PRIVATE_KEY_FUNC callback, PCRYPT_DECRYPT_PRIVATE_KEY_FUNC callback function [Security], security.pcrypt_decrypt_private_key_func, wincrypt/PCRYPT_DECRYPT_PRIVATE_KEY_FUNC
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
 - PCRYPT_DECRYPT_PRIVATE_KEY_FUNC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PCRYPT_DECRYPT_PRIVATE_KEY_FUNC callback function


## -description


<p class="CCE_Message">[The <b>PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</b> function decrypts
the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> and returns the decrypted key in the <i>pbClearTextKey</i> parameter.  <b>PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</b> is a callback function specified in a <a href="https://msdn.microsoft.com/a016e807-60d3-4ae4-829b-43acea2ee8c1">CRYPT_PKCS8_IMPORT_PARAMS</a> structure.  It is used when a  <a href="https://msdn.microsoft.com/5e80d6d1-2e38-4a2d-90df-e6e4000cd626">CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</a> structure contains a private key that needs to be decrypted. The <a href="https://msdn.microsoft.com/fa3deff9-b4c1-4b63-a59f-738f87e1a409">CryptImportPKCS8</a> function uses this function. The function must be implemented by the developer to suit each application.


## -parameters




### -param Algorithm [in]

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that identifies the algorithm used to encrypt the PrivateKeyInfo ASN.1 type found in the PKCS #8 standard.


### -param EncryptedPrivateKey [in]

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a>  value that identifies the encrypted private key  <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a>.


### -param *pbClearTextKey [out]

A pointer to a <b>BYTE</b> buffer to receive the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">plaintext</a>. This parameter can be <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param *pcbClearTextKey [in, out]

A pointer to a  <b>DWORD</b>  value that identifies the size, in  bytes, of the <i>pbClearTextKey</i> buffer. If the size is zero, then <i>pcbClearTextKey</i> should be                  filled with the size, in bytes, required to decrypt the
key, and <i>pbClearTextKey</i> should be ignored.


### -param pVoidDecryptFunc [in]

An <b>LPVOID</b>  value that provides data used in decryption, such as key, initialization vector, and password.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).




## -see-also




<a href="https://msdn.microsoft.com/5e80d6d1-2e38-4a2d-90df-e6e4000cd626">CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</a>



<a href="https://msdn.microsoft.com/a016e807-60d3-4ae4-829b-43acea2ee8c1">CRYPT_PKCS8_IMPORT_PARAMS</a>



<a href="https://msdn.microsoft.com/fa3deff9-b4c1-4b63-a59f-738f87e1a409">CryptImportPKCS8</a>
 

 

