---
UID: NE:d3d12.D3D12_STENCIL_OP
title: D3D12_STENCIL_OP (d3d12.h)
author: windows-sdk-content
description: Identifies the stencil operations that can be performed during depth-stencil testing.
old-location: direct3d12\d3d12_stencil_op.htm
tech.root: direct3d12
ms.assetid: E3527EA4-D931-49C7-B446-829B93A8A620
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_STENCIL_OP, D3D12_STENCIL_OP enumeration, D3D12_STENCIL_OP_DECR, D3D12_STENCIL_OP_DECR_SAT, D3D12_STENCIL_OP_INCR, D3D12_STENCIL_OP_INCR_SAT, D3D12_STENCIL_OP_INVERT, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_REPLACE, D3D12_STENCIL_OP_ZERO, d3d12/D3D12_STENCIL_OP, d3d12/D3D12_STENCIL_OP_DECR, d3d12/D3D12_STENCIL_OP_DECR_SAT, d3d12/D3D12_STENCIL_OP_INCR, d3d12/D3D12_STENCIL_OP_INCR_SAT, d3d12/D3D12_STENCIL_OP_INVERT, d3d12/D3D12_STENCIL_OP_KEEP, d3d12/D3D12_STENCIL_OP_REPLACE, d3d12/D3D12_STENCIL_OP_ZERO, direct3d12.d3d12_stencil_op
ms.topic: enum
f1_keywords: 
 - "d3d12/D3D12_STENCIL_OP"
dev_langs:
 - c++
req.header: d3d12.h
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
 - D3D12.h
api_name:
 - D3D12_STENCIL_OP
targetos: Windows
req.typenames: D3D12_STENCIL_OP
req.redist: 
ms.custom: 19H1
---

# D3D12_STENCIL_OP enumeration


## -description


Identifies the stencil operations that can be performed during depth-stencil testing.


## -enum-fields




### -field D3D12_STENCIL_OP_KEEP

Keep the existing stencil data.


### -field D3D12_STENCIL_OP_ZERO

Set the stencil data to 0.


### -field D3D12_STENCIL_OP_REPLACE

Set the stencil data to the reference value set by calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate">ID3D11DeviceContext::OMSetDepthStencilState</a>.


### -field D3D12_STENCIL_OP_INCR_SAT

Increment the stencil value by 1, and clamp the result.


### -field D3D12_STENCIL_OP_DECR_SAT

Decrement the stencil value by 1, and clamp the result.


### -field D3D12_STENCIL_OP_INVERT

Invert the stencil data.


### -field D3D12_STENCIL_OP_INCR

Increment the stencil value by 1, and wrap the result if necessary.


### -field D3D12_STENCIL_OP_DECR

Decrement the stencil value by 1, and wrap the result if necessary.


## -remarks



This enum is used by the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc">D3D12_DEPTH_STENCILOP_DESC</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/cd3dx12-depth-stencil-desc">CD3DX12_DEPTH_STENCIL_DESC</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
 

 

