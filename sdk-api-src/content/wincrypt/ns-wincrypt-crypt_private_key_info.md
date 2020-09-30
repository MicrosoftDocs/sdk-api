---
UID: NS:wincrypt._CRYPT_PRIVATE_KEY_INFO
title: CRYPT_PRIVATE_KEY_INFO (wincrypt.h)
description: Contains a clear-text private key in the PrivateKey field (DER encoded). CRYPT_PRIVATE_KEY_INFO contains the information in a PKCS
helpviewer_keywords: ["*PCRYPT_PRIVATE_KEY_INFO","CRYPT_PRIVATE_KEY_INFO","CRYPT_PRIVATE_KEY_INFO structure [Security]","PCRYPT_PRIVATE_KEY_INFO","PCRYPT_PRIVATE_KEY_INFO structure pointer [Security]","security.crypt_private_key_info","wincrypt/CRYPT_PRIVATE_KEY_INFO","wincrypt/PCRYPT_PRIVATE_KEY_INFO"]
old-location: security\crypt_private_key_info.htm
tech.root: security
ms.assetid: 63a5d1c2-88b3-45fa-94d3-2179cb8802c9
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PRIVATE_KEY_INFO, CRYPT_PRIVATE_KEY_INFO, CRYPT_PRIVATE_KEY_INFO structure [Security], PCRYPT_PRIVATE_KEY_INFO, PCRYPT_PRIVATE_KEY_INFO structure pointer [Security], security.crypt_private_key_info, wincrypt/CRYPT_PRIVATE_KEY_INFO, wincrypt/PCRYPT_PRIVATE_KEY_INFO'
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
req.typenames: CRYPT_PRIVATE_KEY_INFO, *PCRYPT_PRIVATE_KEY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PRIVATE_KEY_INFO
 - wincrypt/_CRYPT_PRIVATE_KEY_INFO
 - PCRYPT_PRIVATE_KEY_INFO
 - wincrypt/PCRYPT_PRIVATE_KEY_INFO
 - CRYPT_PRIVATE_KEY_INFO
 - wincrypt/CRYPT_PRIVATE_KEY_INFO
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
 - CRYPT_PRIVATE_KEY_INFO
---

# CRYPT_PRIVATE_KEY_INFO structure


## -description

<p class="CCE_Message">[The <b>CRYPT_PRIVATE_KEY_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PRIVATE_KEY_INFO</b> structure contains a clear-text <a href="/windows/desktop/SecGloss/p-gly">private key</a> in the PrivateKey field (DER
   encoded). <b>CRYPT_PRIVATE_KEY_INFO</b> contains the information in a PKCS #8 PrivateKeyInfo ASN.1 type found in the PKCS #8 standard.

## -struct-fields

### -field Version

A <b>DWORD</b>  value that identifies the PKCS #8 version.

### -field Algorithm

A  <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>  structure that indicates the algorithm in which the private key (RSA or DSA) is to be used.

### -field PrivateKey

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a> structure that contains the key data.

### -field pAttributes

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a>  structure that identifies the PKCS #8 attributes.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportpkcs8ex">CryptExportPKCS8Ex</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func">PCRYPT_RESOLVE_HCRYPTPROV_FUNC</a>