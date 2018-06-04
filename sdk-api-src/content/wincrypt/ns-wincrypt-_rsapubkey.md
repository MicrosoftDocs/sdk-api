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

# _RSAPUBKEY structure


## -description


The <b>RSAPUBKEY</b> structure contains information specific to the particular public key contained in the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a>.


## -struct-fields




### -field magic

Set to RSA1 (0x31415352) for public keys and to RSA2 (0x32415352) for private keys. 




<div class="alert"><b>Note</b>  The hexadecimal values are the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> encoding of RSA1 and RSA2.</div>
<div> </div>

### -field bitlen

Number of bits in the modulus. In practice, this must always be a multiple of eight.


### -field pubexp

The public exponent.


## -see-also




<a href="https://msdn.microsoft.com/f0ebab5b-fe86-4604-a7a1-42c6176ac5f3">DSSPUBKEY</a>



<a href="https://msdn.microsoft.com/fbf2b5e4-b572-4b2c-907d-281570a0f26b">DSSSEED</a>



<a href="https://msdn.microsoft.com/99d41222-b4ca-40f3-a240-52b0a9b3a9aa">PUBLICKEYSTRUC</a>
 

 

