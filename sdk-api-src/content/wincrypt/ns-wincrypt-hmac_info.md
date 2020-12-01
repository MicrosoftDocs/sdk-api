---
UID: NS:wincrypt._HMAC_Info
title: HMAC_INFO (wincrypt.h)
description: The HMAC_INFO structure specifies the hash algorithm and the inner and outer strings that are to be used to calculate the HMAC hash.
helpviewer_keywords: ["*PHMAC_INFO","HMAC_INFO","HMAC_INFO structure [Security]","PHMAC_INFO","PHMAC_INFO structure pointer [Security]","_crypto2_hmac_info","security.hmac_info","wincrypt/HMAC_INFO","wincrypt/PHMAC_INFO"]
old-location: security\hmac_info.htm
tech.root: security
ms.assetid: 0c9a9b60-077d-48c0-a5a6-01640cfc0c4e
ms.date: 12/05/2018
ms.keywords: '*PHMAC_INFO, HMAC_INFO, HMAC_INFO structure [Security], PHMAC_INFO, PHMAC_INFO structure pointer [Security], _crypto2_hmac_info, security.hmac_info, wincrypt/HMAC_INFO, wincrypt/PHMAC_INFO'
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
req.typenames: HMAC_INFO, *PHMAC_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HMAC_Info
 - wincrypt/_HMAC_Info
 - PHMAC_INFO
 - wincrypt/PHMAC_INFO
 - HMAC_INFO
 - wincrypt/HMAC_INFO
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
 - HMAC_INFO
---

# HMAC_INFO structure


## -description

The <b>HMAC_INFO</b> structure specifies the <a href="/windows/desktop/SecGloss/h-gly">hash</a> algorithm and the inner and outer strings that are to be used to calculate the <a href="/windows/desktop/SecGloss/h-gly">HMAC</a> hash.

## -struct-fields

### -field HashAlgid

Specifies the hash algorithm to be used.

### -field pbInnerString

A pointer to the inner string to be used in the HMAC calculation. The default inner string is defined as the byte 0x36 repeated 64 times.

### -field cbInnerString

The count of bytes in <b>pbInnerString</b>. The CSP uses the default inner string if <b>cbInnerString</b> is equal to zero.

### -field pbOuterString

A pointer to the outer string to be used in the HMAC calculation. The default outer string is defined as the byte 0x5C repeated 64 times.

### -field cbOuterString

The count of bytes in <b>pbOuterString</b>. The CSP uses the default outer string if <b>cbOuterString</b> is equal to zero.

## -see-also

<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsethashparam">CryptSetHashParam</a>