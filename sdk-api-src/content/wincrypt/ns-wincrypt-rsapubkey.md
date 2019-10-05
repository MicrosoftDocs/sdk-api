---
UID: NS:wincrypt._RSAPUBKEY
title: RSAPUBKEY (wincrypt.h)
author: windows-sdk-content
description: The RSAPUBKEY structure contains information specific to the particular public key contained in the key BLOB.
old-location: security\rsapubkey.htm
tech.root: SecCrypto
ms.assetid: 34b3d591-5d51-484b-accc-9a923d7492b9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RSAPUBKEY, RSAPUBKEY structure [Security], _crypto2_rsapubkey, security.rsapubkey, wincrypt/RSAPUBKEY
ms.topic: struct
f1_keywords:
- wincrypt/RSAPUBKEY
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wincrypt.h
api_name:
- RSAPUBKEY
targetos: Windows
req.typenames: RSAPUBKEY
req.redist: 
ms.custom: 19H1
---

# RSAPUBKEY structure


## -description


The <b>RSAPUBKEY</b> structure contains information specific to the particular public key contained in the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">key BLOB</a>.


## -struct-fields




### -field magic

Set to RSA1 (0x31415352) for public keys and to RSA2 (0x32415352) for private keys. 




<div class="alert"><b>Note</b>  The hexadecimal values are the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">ASCII</a> encoding of RSA1 and RSA2.</div>
<div> </div>

### -field bitlen

Number of bits in the modulus. In practice, this must always be a multiple of eight.


### -field pubexp

The public exponent.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)">DSSPUBKEY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-dssseed">DSSSEED</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-publickeystruc">PUBLICKEYSTRUC</a>
 

 

