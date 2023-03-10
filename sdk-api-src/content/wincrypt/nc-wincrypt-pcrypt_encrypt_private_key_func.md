---
UID: NC:wincrypt.PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC
title: PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC (wincrypt.h)
description: Encrypts the private key and returns the encrypted contents in the pbEncryptedKey parameter.
helpviewer_keywords: ["PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC","PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC callback","PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC callback function [Security]","security.pcrypt_encrypt_private_key_func","wincrypt/PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC"]
old-location: security\pcrypt_encrypt_private_key_func.htm
tech.root: security
ms.assetid: aa6b8bca-4f0d-491e-ab38-5c273a01ca05
ms.date: 12/05/2018
ms.keywords: PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC, PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC callback, PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC callback function [Security], security.pcrypt_encrypt_private_key_func, wincrypt/PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC
 - wincrypt/PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC
---

# PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC callback function


## -description

<p class="CCE_Message">[The <b>PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC</b> function is available for use in  the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC</b> function encrypts the <a href="/windows/desktop/SecGloss/p-gly">private key</a> and returns
the encrypted contents in the <i>pbEncryptedKey</i> parameter.  It is a callback function identified in a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_export_params">CRYPT_PKCS8_EXPORT_PARAMS</a> structure that creates a PKCS #8 <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_encrypted_private_key_info">CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</a> structure.  The function must be implemented by the developer to suit each application.

## -parameters

### -param pAlgorithm [out]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure to receive the algorithm used to encrypt the PrivateKeyInfo ASN.1 type found in the PKCS #8 standard.

### -param pClearTextPrivateKey [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains the <a href="/windows/desktop/SecGloss/p-gly">plaintext</a> private key to be encrypted.

### -param pbEncryptedKey [out]

A pointer to a <b>BYTE</b> buffer to receive the encrypted <a href="/windows/desktop/SecGloss/p-gly">private key BLOB</a>. If this parameter is <b>NULL</b>, <i>pcbEncryptedKey</i> will return the size, in bytes, of memory needed to contain the encrypted key on a subsequent call to this function.

### -param pcbEncryptedKey [in, out]

A pointer to a <b>DWORD</b>  variable that contains the size, in  bytes, of the <i>pbEncryptedKey</i> buffer. If pbEncryptedKey is  <b>NULL</b>, then <i>pcbEncryptedKey</i>  is
set to the size, in bytes,  required to encrypt the
key. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pVoidEncryptFunc [in]

An  <b>LPVOID</b> variable that contains data used for encryption, such as key, initialization vector, and password.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).


If the function fails, it returns zero (<b>FALSE</b>).

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_export_params">CRYPT_PKCS8_EXPORT_PARAMS</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a>
