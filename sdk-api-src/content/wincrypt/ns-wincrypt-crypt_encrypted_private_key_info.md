---
UID: NS:wincrypt._CRYPT_ENCRYPTED_PRIVATE_KEY_INFO
title: CRYPT_ENCRYPTED_PRIVATE_KEY_INFO (wincrypt.h)
description: Contains the information in a PKCS
helpviewer_keywords: ["*PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO","CRYPT_ENCRYPTED_PRIVATE_KEY_INFO","CRYPT_ENCRYPTED_PRIVATE_KEY_INFO structure [Security]","PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO","PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO structure pointer [Security]","security.crypt_encrypted_private_key_info","wincrypt/CRYPT_ENCRYPTED_PRIVATE_KEY_INFO","wincrypt/PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO"]
old-location: security\crypt_encrypted_private_key_info.htm
tech.root: security
ms.assetid: 5e80d6d1-2e38-4a2d-90df-e6e4000cd626
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO, CRYPT_ENCRYPTED_PRIVATE_KEY_INFO, CRYPT_ENCRYPTED_PRIVATE_KEY_INFO structure [Security], PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO, PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO structure pointer [Security], security.crypt_encrypted_private_key_info, wincrypt/CRYPT_ENCRYPTED_PRIVATE_KEY_INFO, wincrypt/PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO'
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
req.typenames: CRYPT_ENCRYPTED_PRIVATE_KEY_INFO, *PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_ENCRYPTED_PRIVATE_KEY_INFO
 - wincrypt/_CRYPT_ENCRYPTED_PRIVATE_KEY_INFO
 - PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO
 - wincrypt/PCRYPT_ENCRYPTED_PRIVATE_KEY_INFO
 - CRYPT_ENCRYPTED_PRIVATE_KEY_INFO
 - wincrypt/CRYPT_ENCRYPTED_PRIVATE_KEY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_ENCRYPTED_PRIVATE_KEY_INFO
---

# CRYPT_ENCRYPTED_PRIVATE_KEY_INFO structure


## -description

<p class="CCE_Message">[The <b>CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_ENCRYPTED_PRIVATE_KEY_INFO</b> structure contains the information in a PKCS #8
EncryptedPrivateKeyInfo ASN.1 type found in the PKCS #8 standard.

## -struct-fields

### -field EncryptionAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that indicates the algorithm used for encryption.

### -field EncryptedPrivateKey

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains the encrypted private key data.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportpkcs8ex">CryptExportPKCS8Ex</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_encrypt_private_key_func">PCRYPT_ENCRYPT_PRIVATE_KEY_FUNC</a>