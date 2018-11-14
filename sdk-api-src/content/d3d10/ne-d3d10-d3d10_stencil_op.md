---
UID: NE:d3d10.D3D10_STENCIL_OP
title: D3D10_STENCIL_OP
author: windows-sdk-content
description: The stencil operations that can be performed during depth-stencil testing.
old-location: direct3d10\d3d10_stencil_op.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_stencil_op.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 8b95cc96-2219-8855-744f-f4663f6c19b8, D3D10_STENCIL_OP, D3D10_STENCIL_OP enumeration [Direct3D 10], D3D10_STENCIL_OP_DECR, D3D10_STENCIL_OP_DECR_SAT, D3D10_STENCIL_OP_INCR, D3D10_STENCIL_OP_INCR_SAT, D3D10_STENCIL_OP_INVERT, D3D10_STENCIL_OP_KEEP, D3D10_STENCIL_OP_REPLACE, D3D10_STENCIL_OP_ZERO, d3d10/D3D10_STENCIL_OP, d3d10/D3D10_STENCIL_OP_DECR, d3d10/D3D10_STENCIL_OP_DECR_SAT, d3d10/D3D10_STENCIL_OP_INCR, d3d10/D3D10_STENCIL_OP_INCR_SAT, d3d10/D3D10_STENCIL_OP_INVERT, d3d10/D3D10_STENCIL_OP_KEEP, d3d10/D3D10_STENCIL_OP_REPLACE, d3d10/D3D10_STENCIL_OP_ZERO, direct3d10.d3d10_stencil_op
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_STENCIL_OP
product: Windows
targetos: Windows
req.typenames: D3D10_STENCIL_OP
req.redist: 
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
 

 

