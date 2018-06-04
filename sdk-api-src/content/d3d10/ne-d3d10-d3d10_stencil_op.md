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

# D3D10_STENCIL_OP enumeration


## -description


The stencil operations that can be performed during <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">depth-stencil</a> testing.


## -enum-fields




### -field D3D10_STENCIL_OP_KEEP

Keep the existing stencil data.


### -field D3D10_STENCIL_OP_ZERO

Set the stencil data to 0.


### -field D3D10_STENCIL_OP_REPLACE

Set the stencil data to the reference value set by calling <a href="https://msdn.microsoft.com/7cf8e5ca-08f2-4fa3-8657-cbce5d773dcf">ID3D10Device::OMSetDepthStencilState</a>.


### -field D3D10_STENCIL_OP_INCR_SAT

Increment the stencil value by 1, and clamp the result.


### -field D3D10_STENCIL_OP_DECR_SAT

Decrement the stencil value by 1, and clamp the result.


### -field D3D10_STENCIL_OP_INVERT

Invert the stencil data.


### -field D3D10_STENCIL_OP_INCR

Increment the stencil value by 1, and wrap the result if necessary.


### -field D3D10_STENCIL_OP_DECR

Increment the stencil value by 1, and wrap the result if necessary.


## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

