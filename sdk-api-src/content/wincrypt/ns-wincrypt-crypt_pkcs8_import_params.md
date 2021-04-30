---
UID: NS:wincrypt._CRYPT_PKCS8_IMPORT_PARAMS
title: CRYPT_PKCS8_IMPORT_PARAMS (wincrypt.h)
description: Contains a PKCS
helpviewer_keywords: ["*PCRYPT_PKCS8_IMPORT_PARAMS","*PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS","CRYPT_PKCS8_IMPORT_PARAMS","CRYPT_PKCS8_IMPORT_PARAMS structure [Security]","CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS","CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS structure [Security]","PCRYPT_PKCS8_IMPORT_PARAMS","PCRYPT_PKCS8_IMPORT_PARAMS structure pointer [Security]","PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS","PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS structure pointer [Security]","security.crypt_pkcs8_import_params","wincrypt/CRYPT_PKCS8_IMPORT_PARAMS","wincrypt/CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS","wincrypt/PCRYPT_PKCS8_IMPORT_PARAMS","wincrypt/PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS"]
old-location: security\crypt_pkcs8_import_params.htm
tech.root: security
ms.assetid: a016e807-60d3-4ae4-829b-43acea2ee8c1
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PKCS8_IMPORT_PARAMS, *PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS, CRYPT_PKCS8_IMPORT_PARAMS, CRYPT_PKCS8_IMPORT_PARAMS structure [Security], CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS, CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS structure [Security], PCRYPT_PKCS8_IMPORT_PARAMS, PCRYPT_PKCS8_IMPORT_PARAMS structure pointer [Security], PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS, PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS structure pointer [Security], security.crypt_pkcs8_import_params, wincrypt/CRYPT_PKCS8_IMPORT_PARAMS, wincrypt/CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS, wincrypt/PCRYPT_PKCS8_IMPORT_PARAMS, wincrypt/PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS'
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
req.typenames: CRYPT_PKCS8_IMPORT_PARAMS, *PCRYPT_PKCS8_IMPORT_PARAMS, CRYPT_PRIVATE_KEY_BLOB_AND_PARAMS, *PCRYPT_PRIVATE_KEY_BLOB_AND_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PKCS8_IMPORT_PARAMS
 - wincrypt/_CRYPT_PKCS8_IMPORT_PARAMS
 - PCRYPT_PKCS8_IMPORT_PARAMS
 - wincrypt/PCRYPT_PKCS8_IMPORT_PARAMS
 - CRYPT_PKCS8_IMPORT_PARAMS
 - wincrypt/CRYPT_PKCS8_IMPORT_PARAMS
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
 - CRYPT_PKCS8_IMPORT_PARAMS
---

# CRYPT_PKCS8_IMPORT_PARAMS structure


## -description

<p class="CCE_Message">[The <b>CRYPT_PKCS8_IMPORT_PARAMS</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PKCS8_IMPORT_PARAMS</b> structure contains a PKCS #8 <a href="/windows/desktop/SecGloss/p-gly">private key</a> and pointers to callback
functions. <b>CRYPT_PKCS8_IMPORT_PARAMS</b> is used by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpkcs8">CryptImportPKCS8</a> function. The first callback supplies the algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and <a href="/windows/desktop/SecGloss/k-gly">key length</a> needed to  specify the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) into which the key will be imported. If the private key in PKCS #8 is encrypted, the <b>CRYPT_PKCS8_IMPORT_PARAMS</b> structure contains the encrypted private key, and the second callback is used to decrypt this private key.

## -struct-fields

### -field PrivateKey

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DIGEST_BLOB</a> structure that contains the PKCS #8 data.

### -field pResolvehCryptProvFunc

A <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func">PCRYPT_RESOLVE_HCRYPTPROV_FUNC</a> pointer  that points to data used by a user-defined function that retrieves a handle to a CSP.

### -field pVoidResolveFunc

An  <b>LPVOID</b>  value that identifies the function used to retrieve the CSP provider handle.

### -field pDecryptPrivateKeyFunc

A <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a> pointer that points to  a callback function used to decrypt the private key.

### -field pVoidDecryptFunc

An <b>LPVOID</b> value that provides data used for encryption, such as key, initialization vector, and password.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportpkcs8ex">CryptExportPKCS8Ex</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpkcs8">CryptImportPKCS8</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func">PCRYPT_DECRYPT_PRIVATE_KEY_FUNC</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func">PCRYPT_RESOLVE_HCRYPTPROV_FUNC</a>