---
UID: NS:wincrypt._DSSSEED
title: "_DSSSEED"
author: windows-driver-content
description: Holds the seed and counter values that can be used to verify the primes of the DSS public key.
old-location: security\dssseed.htm
old-project: SecCrypto
ms.assetid: fbf2b5e4-b572-4b2c-907d-281570a0f26b
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: DSSSEED, DSSSEED structure [Security], _DSSSEED, _crypto2_dssseed, security.dssseed, wincrypt/DSSSEED
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DSSSEED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	DSSSEED
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DSSSEED structure


## -description


The <b>DSSSEED</b> structure holds the seed and counter values that can be used to verify the primes of the DSS public key.


## -struct-fields




### -field counter

A <b>DWORD</b> containing the counter value. If the counter value is 0xFFFFFFFF, the seed and counter values are not available.


### -field seed

A <b>BYTE</b> string containing the seed value.


## -see-also




<a href="https://msdn.microsoft.com/f0ebab5b-fe86-4604-a7a1-42c6176ac5f3">DSSPUBKEY</a>



<a href="https://msdn.microsoft.com/99d41222-b4ca-40f3-a240-52b0a9b3a9aa">PUBLICKEYSTRUC</a>



<a href="https://msdn.microsoft.com/34b3d591-5d51-484b-accc-9a923d7492b9">RSAPUBKEY</a>
 

 

