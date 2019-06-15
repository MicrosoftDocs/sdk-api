---
UID: NS:wincrypt._DSSSEED
title: DSSSEED (wincrypt.h)
author: windows-sdk-content
description: Holds the seed and counter values that can be used to verify the primes of the DSS public key.
old-location: security\dssseed.htm
tech.root: SecCrypto
ms.assetid: fbf2b5e4-b572-4b2c-907d-281570a0f26b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DSSSEED, DSSSEED structure [Security], _crypto2_dssseed, security.dssseed, wincrypt/DSSSEED
ms.topic: struct
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
 - DSSSEED
product: Windows
targetos: Windows
req.typenames: DSSSEED
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)">DSSPUBKEY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_publickeystruc">PUBLICKEYSTRUC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_rsapubkey">RSAPUBKEY</a>
 

 

