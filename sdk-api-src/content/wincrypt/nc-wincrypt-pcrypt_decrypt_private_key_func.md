---
UID: NC:wincrypt.PCRYPT_DECRYPT_PRIVATE_KEY_FUNC
title: PCRYPT_DECRYPT_PRIVATE_KEY_FUNC (wincrypt.h)
description: Decrypts the private key and returns the decrypted key in the pbClearTextKey parameter.
helpviewer_keywords: ["PCRYPT_DECRYPT_PRIVATE_KEY_FUNC","PCRYPT_DECRYPT_PRIVATE_KEY_FUNC callback","PCRYPT_DECRYPT_PRIVATE_KEY_FUNC callback function [Security]","security.pcrypt_decrypt_private_key_func","wincrypt/PCRYPT_DECRYPT_PRIVATE_KEY_FUNC"]
old-location: security\pcrypt_decrypt_private_key_func.htm
tech.root: security
ms.assetid: f59fd46b-5430-4aa2-85ba-961b416dbaac
ms.date: 12/05/2018
ms.keywords: PCRYPT_DECRYPT_PRIVATE_KEY_FUNC, PCRYPT_DECRYPT_PRIVATE_KEY_FUNC callback, PCRYPT_DECRYPT_PRIVATE_KEY_FUNC callback function [Security], security.pcrypt_decrypt_private_key_func, wincrypt/PCRYPT_DECRYPT_PRIVATE_KEY_FUNC
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
 - PCRYPT_DECRYPT_PRIVATE_KEY_FUNC
 - wincrypt/PCRYPT_DECRYPT_PRIVATE_KEY_FUNC
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
 - PCRYPT_DECRYPT_PRIVATE_KEY_FUNC
---

# PCRYPT_DECRYPT_PRIVATE_KEY_FUNC callback function


## -description

<p class="CCE_Message">[The <b>PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</b> function decrypts
the <a href="/windows/desktop/SecGloss/p-gly">private key</a> and returns the decrypted key in the <i>pbClearTextKey</i> parameter.  <b>PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</b> is a callback function specified in a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_import_params">CRYPT_PKCS8_IMPORT_PARAMS</a> structure.  It is used when a  <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_encrypted_private_key_info">CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</a> structure contains a private key that needs to be decrypted. The <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpkcs8">CryptImportPKCS8</a> function uses this function. The function must be implemented by the developer to suit each application.

## -parameters

### -param Algorithm [in]

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that identifies the algorithm used to encrypt the PrivateKeyInfo ASN.1 type found in the PKCS #8 standard.

### -param EncryptedPrivateKey [in]

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>  value that identifies the encrypted private key  <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.

### -param pbClearTextKey [out]

A pointer to a <b>BYTE</b> buffer to receive the <a href="/windows/desktop/SecGloss/p-gly">plaintext</a>. This parameter can be <b>NULL</b>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbClearTextKey [in, out]

A pointer to a  <b>DWORD</b>  value that identifies the size, in  bytes, of the <i>pbClearTextKey</i> buffer. If the size is zero, then <i>pcbClearTextKey</i> should be                  filled with the size, in bytes, required to decrypt the
key, and <i>pbClearTextKey</i> should be ignored.

### -param pVoidDecryptFunc [in]

An <b>LPVOID</b>  value that provides data used in decryption, such as key, initialization vector, and password.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_encrypted_private_key_info">CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_import_params">CRYPT_PKCS8_IMPORT_PARAMS</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpkcs8">CryptImportPKCS8</a>
