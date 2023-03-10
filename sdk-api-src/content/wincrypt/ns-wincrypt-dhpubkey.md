---
UID: NS:wincrypt._PUBKEY
title: DHPUBKEY (wincrypt.h)
description: Contains information specific to the particular Diffie-Hellman public key contained in the key BLOB.
helpviewer_keywords: ["DHPUBKEY","DHPUBKEY structure [Security]","DSSPUBKEY","KEAPUBKEY","TEKPUBKEY","_PUBKEY","_crypto2_dhpubkey","security.dhpubkey","wincrypt/DHPUBKEY"]
old-location: security\dhpubkey.htm
tech.root: security
ms.assetid: 12fb2e81-796d-4501-91b5-ee572a3293bb
ms.date: 12/05/2018
ms.keywords: DHPUBKEY, DHPUBKEY structure [Security], DSSPUBKEY, KEAPUBKEY, TEKPUBKEY, _PUBKEY, _crypto2_dhpubkey, security.dhpubkey, wincrypt/DHPUBKEY
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
req.typenames: DHPUBKEY, DSSPUBKEY, KEAPUBKEY, TEKPUBKEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PUBKEY
 - wincrypt/_PUBKEY
 - DHPUBKEY
 - wincrypt/DHPUBKEY
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
 - DHPUBKEY
---

# DHPUBKEY structure


## -description

The <b>DHPUBKEY</b> structure contains information specific to the particular Diffie-Hellman <a href="/windows/desktop/SecGloss/p-gly">public key</a> contained in the <a href="/windows/desktop/SecGloss/k-gly">key BLOB</a>.

## -struct-fields

### -field magic

This must always be set to DH1 (0x31484400) when used for <a href="/windows/desktop/SecGloss/p-gly">public key BLOBs</a> and to DH2 (0x32484400) when used for <a href="/windows/desktop/SecGloss/p-gly">private key BLOBs</a>. 




Notice that the hexadecimal values are simply an <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> encoding of DH1 and DH2.

### -field bitlen

Number of bits in the prime modulus, P.

## -remarks

<b>DSSPUBKEY</b> is an alias for this structure.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-publickeystruc">PUBLICKEYSTRUC</a>