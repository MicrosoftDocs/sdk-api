---
UID: NC:wincrypt.PCRYPT_RESOLVE_HCRYPTPROV_FUNC
title: PCRYPT_RESOLVE_HCRYPTPROV_FUNC (wincrypt.h)
description: Returns a handle to a cryptographic service provider (CSP) by using the phCryptProv parameter to receive the key being imported.
helpviewer_keywords: ["PCRYPT_RESOLVE_HCRYPTPROV_FUNC","PCRYPT_RESOLVE_HCRYPTPROV_FUNC callback","PCRYPT_RESOLVE_HCRYPTPROV_FUNC callback function [Security]","security.pcrypt_resolve_hcryptprov_func","wincrypt/PCRYPT_RESOLVE_HCRYPTPROV_FUNC"]
old-location: security\pcrypt_resolve_hcryptprov_func.htm
tech.root: security
ms.assetid: d3b2b942-bde5-4399-9412-95fe227cd546
ms.date: 12/05/2018
ms.keywords: PCRYPT_RESOLVE_HCRYPTPROV_FUNC, PCRYPT_RESOLVE_HCRYPTPROV_FUNC callback, PCRYPT_RESOLVE_HCRYPTPROV_FUNC callback function [Security], security.pcrypt_resolve_hcryptprov_func, wincrypt/PCRYPT_RESOLVE_HCRYPTPROV_FUNC
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
 - PCRYPT_RESOLVE_HCRYPTPROV_FUNC
 - wincrypt/PCRYPT_RESOLVE_HCRYPTPROV_FUNC
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
 - PCRYPT_RESOLVE_HCRYPTPROV_FUNC
---

# PCRYPT_RESOLVE_HCRYPTPROV_FUNC callback function


## -description

<p class="CCE_Message">[The <b>PCRYPT_RESOLVE_HCRYPTPROV_FUNC</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>PCRYPT_RESOLVE_HCRYPTPROV_FUNC</b> function returns a handle to a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) by using the <i>phCryptProv</i> parameter to receive the key being imported.  It is a callback function called from the context of  the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpkcs8">CryptImportPKCS8</a> function.  The function must be implemented by the developer to suit each application.

## -parameters

### -param pPrivateKeyInfo [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_private_key_info">CRYPT_PRIVATE_KEY_INFO</a> structure that describes the key being imported.

### -param phCryptProv [out]

A pointer to the  <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a>   to receive the CSP.

### -param pVoidResolveFunc [in]

The <b>pVoidResolveFunc</b> member passed in by the caller in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_import_params">CRYPT_PKCS8_IMPORT_PARAMS</a>  structure.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_pkcs8_import_params">CRYPT_PKCS8_IMPORT_PARAMS</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_private_key_info">CRYPT_PRIVATE_KEY_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpkcs8">CryptImportPKCS8</a>



<a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a>
