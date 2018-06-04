---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _PRIVKEYVER3 structure


## -description


The <b>DHPRIVKEY_VER3</b> structure contains information specific to the particular <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> contained in the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a>.


## -struct-fields




### -field magic

This must always be set to 0x34484400, the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> encoding of "DH4".


### -field bitlenP

Number of bits in the DH key BLOB's prime, P.


### -field bitlenQ

Number of bits in the DH key BLOB's prime, Q. If Q is not available then this value should be 0.


### -field bitlenJ

Number of bits in the DH key BLOB's prime, J. If J is not in the BLOB, then this value should be 0.


### -field bitlenX

Number of bits in the DH key BLOB private exponent, X.


### -field DSSSeed

Seed structure holding the seed and counter values used to generate the primes Q and P. If values in the <a href="https://msdn.microsoft.com/fbf2b5e4-b572-4b2c-907d-281570a0f26b">DSSSEED</a> structure are not available, then the counter element of the structure should be 0xFFFFFFFF.


## -see-also




<a href="https://msdn.microsoft.com/99d41222-b4ca-40f3-a240-52b0a9b3a9aa">BLOBHEADER</a>



<a href="https://msdn.microsoft.com/fbf2b5e4-b572-4b2c-907d-281570a0f26b">DSSSEED</a>
 

 

