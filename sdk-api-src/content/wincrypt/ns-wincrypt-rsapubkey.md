---
UID: NS:wincrypt._RSAPUBKEY
title: RSAPUBKEY (wincrypt.h)
description: The RSAPUBKEY structure contains information specific to the particular public key contained in the key BLOB.
helpviewer_keywords: ["RSAPUBKEY","RSAPUBKEY structure [Security]","_crypto2_rsapubkey","security.rsapubkey","wincrypt/RSAPUBKEY"]
old-location: security\rsapubkey.htm
tech.root: security
ms.assetid: 34b3d591-5d51-484b-accc-9a923d7492b9
ms.date: 12/05/2018
ms.keywords: RSAPUBKEY, RSAPUBKEY structure [Security], _crypto2_rsapubkey, security.rsapubkey, wincrypt/RSAPUBKEY
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
req.typenames: RSAPUBKEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RSAPUBKEY
 - wincrypt/_RSAPUBKEY
 - RSAPUBKEY
 - wincrypt/RSAPUBKEY
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
 - RSAPUBKEY
---

# RSAPUBKEY structure


## -description

The <b>RSAPUBKEY</b> structure contains information specific to the particular public key contained in the <a href="/windows/desktop/SecGloss/k-gly">key BLOB</a>.

## -struct-fields

### -field magic

Set to RSA1 (0x31415352) for public keys and to RSA2 (0x32415352) for private keys. 




<div class="alert"><b>Note</b>  The hexadecimal values are the <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> encoding of RSA1 and RSA2.</div>
<div> </div>

### -field bitlen

Number of bits in the modulus. In practice, this must always be a multiple of eight.

### -field pubexp

The public exponent.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)">DSSPUBKEY</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-dssseed">DSSSEED</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-publickeystruc">PUBLICKEYSTRUC</a>