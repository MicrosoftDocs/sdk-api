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
 

 

