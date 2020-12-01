---
UID: NS:wincrypt._PUBKEYVER3
title: DHPUBKEY_VER3 (wincrypt.h)
description: Contains information specific to the particular public key contained in the key BLOB.
helpviewer_keywords: ["DHPUBKEY_VER3","DHPUBKEY_VER3 structure [Security]","DSSPUBKEY_VER3","_PUBKEYVER3","_crypto2_dhpubkey_ver3","security.dhpubkey_ver3","wincrypt/DHPUBKEY_VER3"]
old-location: security\dhpubkey_ver3.htm
tech.root: security
ms.assetid: 02f702dd-be9d-4a9a-a3af-4db1802386b0
ms.date: 12/05/2018
ms.keywords: DHPUBKEY_VER3, DHPUBKEY_VER3 structure [Security], DSSPUBKEY_VER3, _PUBKEYVER3, _crypto2_dhpubkey_ver3, security.dhpubkey_ver3, wincrypt/DHPUBKEY_VER3
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
req.typenames: DHPUBKEY_VER3, DSSPUBKEY_VER3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PUBKEYVER3
 - wincrypt/_PUBKEYVER3
 - DHPUBKEY_VER3
 - wincrypt/DHPUBKEY_VER3
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
 - DHPUBKEY_VER3
---

# DHPUBKEY_VER3 structure


## -description

The <b>DHPUBKEY_VER3</b> structure contains information specific to the particular <a href="/windows/desktop/SecGloss/p-gly">public key</a> contained in the <a href="/windows/desktop/SecGloss/k-gly">key BLOB</a>.

## -struct-fields

### -field magic

This must always be set to 0x33484400, the <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> encoding of "DH3".

### -field bitlenP

Number of bits in the DH key BLOB's prime, P.

### -field bitlenQ

Number of bits in the DH key BLOB's prime, Q. If Q is not available, then this value should be 0.

### -field bitlenJ

Number of bits in the DH key BLOB's prime, J. If J is not in the BLOB, then this value should be 0.

### -field DSSSeed

Seed structure holding the seed and counter values used to generate the primes Q and P. If values in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-dssseed">DSSSEED</a> structure are not available, then the counter element of the structure should be 0xFFFFFFFF.

## -remarks

<b>DSSPUBKEY_VER3</b> is an alias for this structure.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-publickeystruc">BLOBHEADER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-dssseed">DSSSEED</a>