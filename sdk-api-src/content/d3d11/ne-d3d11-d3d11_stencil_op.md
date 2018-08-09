---
UID: NE:d3d11.D3D11_STENCIL_OP
title: D3D11_STENCIL_OP
author: windows-sdk-content
description: The stencil operations that can be performed during depth-stencil testing.
old-location: direct3d11\d3d11_stencil_op.htm
old-project: direct3d11
ms.assetid: 4a08ce69-a3e1-43d3-bf7e-e14b106fbecf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 040086f5-0f64-f459-6184-d4091d98d3d4, D3D11_STENCIL_OP, D3D11_STENCIL_OP enumeration [Direct3D 11], D3D11_STENCIL_OP_DECR, D3D11_STENCIL_OP_DECR_SAT, D3D11_STENCIL_OP_INCR, D3D11_STENCIL_OP_INCR_SAT, D3D11_STENCIL_OP_INVERT, D3D11_STENCIL_OP_KEEP, D3D11_STENCIL_OP_REPLACE, D3D11_STENCIL_OP_ZERO, d3d11/D3D11_STENCIL_OP, d3d11/D3D11_STENCIL_OP_DECR, d3d11/D3D11_STENCIL_OP_DECR_SAT, d3d11/D3D11_STENCIL_OP_INCR, d3d11/D3D11_STENCIL_OP_INCR_SAT, d3d11/D3D11_STENCIL_OP_INVERT, d3d11/D3D11_STENCIL_OP_KEEP, d3d11/D3D11_STENCIL_OP_REPLACE, d3d11/D3D11_STENCIL_OP_ZERO, direct3d11.d3d11_stencil_op
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11.h
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
tech.root: 
req.typenames: D3D11_STENCIL_OP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_STENCIL_OP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_STENCIL_OP enumeration


## -description


The stencil operations that can be performed during depth-stencil testing.


## -enum-fields




### -field D3D11_STENCIL_OP_KEEP

Keep the existing stencil data.


### -field D3D11_STENCIL_OP_ZERO

Set the stencil data to 0.


### -field D3D11_STENCIL_OP_REPLACE

Set the stencil data to the reference value set by calling <a href="https://msdn.microsoft.com/cd5642c4-8bbe-4b5d-9f04-87de82ee9601">ID3D11DeviceContext::OMSetDepthStencilState</a>.


### -field D3D11_STENCIL_OP_INCR_SAT

Increment the stencil value by 1, and clamp the result.


### -field D3D11_STENCIL_OP_DECR_SAT

Decrement the stencil value by 1, and clamp the result.


### -field D3D11_STENCIL_OP_INVERT

Invert the stencil data.


### -field D3D11_STENCIL_OP_INCR

Increment the stencil value by 1, and wrap the result if necessary.


### -field D3D11_STENCIL_OP_DECR

Decrement the stencil value by 1, and wrap the result if necessary.


## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

