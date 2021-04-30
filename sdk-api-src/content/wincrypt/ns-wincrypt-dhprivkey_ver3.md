---
UID: NS:wincrypt._PRIVKEYVER3
title: DHPRIVKEY_VER3 (wincrypt.h)
description: Contains information specific to the particular private key contained in the key BLOB.
helpviewer_keywords: ["DHPRIVKEY_VER3","DHPRIVKEY_VER3 structure [Security]","DSSPRIVKEY_VER3","_PRIVKEYVER3","_crypto2_dhprivkey_ver3","security.dhprivkey_ver3","wincrypt/DHPRIVKEY_VER3"]
old-location: security\dhprivkey_ver3.htm
tech.root: security
ms.assetid: ad4bf20d-5c6c-4373-bd88-9a5bbb832ba5
ms.date: 12/05/2018
ms.keywords: DHPRIVKEY_VER3, DHPRIVKEY_VER3 structure [Security], DSSPRIVKEY_VER3, _PRIVKEYVER3, _crypto2_dhprivkey_ver3, security.dhprivkey_ver3, wincrypt/DHPRIVKEY_VER3
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
req.typenames: DHPRIVKEY_VER3, DSSPRIVKEY_VER3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PRIVKEYVER3
 - wincrypt/_PRIVKEYVER3
 - DHPRIVKEY_VER3
 - wincrypt/DHPRIVKEY_VER3
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
 - DHPRIVKEY_VER3
---

# DHPRIVKEY_VER3 structure


## -description

The <b>DHPRIVKEY_VER3</b> structure contains information specific to the particular <a href="/windows/desktop/SecGloss/p-gly">private key</a> contained in the <a href="/windows/desktop/SecGloss/k-gly">key BLOB</a>.

## -struct-fields

### -field magic

This must always be set to 0x34484400, the <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> encoding of "DH4".

### -field bitlenP

Number of bits in the DH key BLOB's prime, P.

### -field bitlenQ

Number of bits in the DH key BLOB's prime, Q. If Q is not available then this value should be 0.

### -field bitlenJ

Number of bits in the DH key BLOB's prime, J. If J is not in the BLOB, then this value should be 0.

### -field bitlenX

Number of bits in the DH key BLOB private exponent, X.

### -field DSSSeed

Seed structure holding the seed and counter values used to generate the primes Q and P. If values in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-dssseed">DSSSEED</a> structure are not available, then the counter element of the structure should be 0xFFFFFFFF.

## -remarks

<b>DSSPRIVKEY_VER3</b> is an alias for this structure.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-publickeystruc">BLOBHEADER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-dssseed">DSSSEED</a>