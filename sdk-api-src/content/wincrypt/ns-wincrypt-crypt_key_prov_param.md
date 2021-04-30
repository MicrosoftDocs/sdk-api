---
UID: NS:wincrypt._CRYPT_KEY_PROV_PARAM
title: CRYPT_KEY_PROV_PARAM (wincrypt.h)
description: Contains information about a key container parameter.
helpviewer_keywords: ["*PCRYPT_KEY_PROV_PARAM","CRYPT_KEY_PROV_PARAM","CRYPT_KEY_PROV_PARAM structure [Security]","PCRYPT_KEY_PROV_PARAM","PCRYPT_KEY_PROV_PARAM structure pointer [Security]","_crypto2_crypt_key_prov_param","security.crypt_key_prov_param","wincrypt/CRYPT_KEY_PROV_PARAM","wincrypt/PCRYPT_KEY_PROV_PARAM"]
old-location: security\crypt_key_prov_param.htm
tech.root: security
ms.assetid: 3731708f-0ce9-42bf-ace9-5ed671be113a
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_KEY_PROV_PARAM, CRYPT_KEY_PROV_PARAM, CRYPT_KEY_PROV_PARAM structure [Security], PCRYPT_KEY_PROV_PARAM, PCRYPT_KEY_PROV_PARAM structure pointer [Security], _crypto2_crypt_key_prov_param, security.crypt_key_prov_param, wincrypt/CRYPT_KEY_PROV_PARAM, wincrypt/PCRYPT_KEY_PROV_PARAM'
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
req.typenames: CRYPT_KEY_PROV_PARAM, *PCRYPT_KEY_PROV_PARAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_KEY_PROV_PARAM
 - wincrypt/_CRYPT_KEY_PROV_PARAM
 - PCRYPT_KEY_PROV_PARAM
 - wincrypt/PCRYPT_KEY_PROV_PARAM
 - CRYPT_KEY_PROV_PARAM
 - wincrypt/CRYPT_KEY_PROV_PARAM
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
 - CRYPT_KEY_PROV_PARAM
---

# CRYPT_KEY_PROV_PARAM structure


## -description

The <b>CRYPT_KEY_PROV_PARAM</b> structure contains information about a <a href="/windows/desktop/SecGloss/k-gly">key container</a> parameter. This structure is used with the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure.

## -struct-fields

### -field dwParam

Identifies the parameter. For possible values, see the <i>dwParam</i> parameter of the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a> function.

### -field pbData

The address of a buffer that contains the parameter data. For more information, see the <i>pbData</i> parameter of the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a> function.

### -field cbData

The size, in bytes, of the <b>pbData</b> buffer.

### -field dwFlags

This member is reserved for future use and is zero.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetprovparam">CryptSetProvParam</a>