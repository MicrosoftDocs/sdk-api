---
UID: NS:wincrypt._DSSSEED
title: DSSSEED (wincrypt.h)
description: Holds the seed and counter values that can be used to verify the primes of the DSS public key.
helpviewer_keywords: ["DSSSEED","DSSSEED structure [Security]","_crypto2_dssseed","security.dssseed","wincrypt/DSSSEED"]
old-location: security\dssseed.htm
tech.root: security
ms.assetid: fbf2b5e4-b572-4b2c-907d-281570a0f26b
ms.date: 12/05/2018
ms.keywords: DSSSEED, DSSSEED structure [Security], _crypto2_dssseed, security.dssseed, wincrypt/DSSSEED
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
req.typenames: DSSSEED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSSSEED
 - wincrypt/_DSSSEED
 - DSSSEED
 - wincrypt/DSSSEED
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
 - DSSSEED
---

# DSSSEED structure


## -description

The <b>DSSSEED</b> structure holds the seed and counter values that can be used to verify the primes of the DSS public key.

## -struct-fields

### -field counter

A <b>DWORD</b> containing the counter value. If the counter value is 0xFFFFFFFF, the seed and counter values are not available.

### -field seed

A <b>BYTE</b> string containing the seed value.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)">DSSPUBKEY</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-publickeystruc">PUBLICKEYSTRUC</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-rsapubkey">RSAPUBKEY</a>