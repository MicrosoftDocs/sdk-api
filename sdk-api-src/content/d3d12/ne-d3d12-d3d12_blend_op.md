---
UID: NE:d3d12.D3D12_BLEND_OP
title: D3D12_BLEND_OP (d3d12.h)
author: windows-sdk-content
description: Specifies RGB or alpha blending operations.
old-location: direct3d12\d3d12_blend_op.htm
tech.root: direct3d12
ms.assetid: 2C36BFCB-2871-446F-8A79-3E963DB50795
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_BLEND_OP, D3D12_BLEND_OP enumeration, D3D12_BLEND_OP_ADD, D3D12_BLEND_OP_MAX, D3D12_BLEND_OP_MIN, D3D12_BLEND_OP_REV_SUBTRACT, D3D12_BLEND_OP_SUBTRACT, d3d12/D3D12_BLEND_OP, d3d12/D3D12_BLEND_OP_ADD, d3d12/D3D12_BLEND_OP_MAX, d3d12/D3D12_BLEND_OP_MIN, d3d12/D3D12_BLEND_OP_REV_SUBTRACT, d3d12/D3D12_BLEND_OP_SUBTRACT, direct3d12.d3d12_blend_op
ms.topic: enum
f1_keywords: ["d3d12/D3D12_BLEND_OP"]
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
 - D3D12_BLEND_OP
product: Windows
targetos: Windows
req.typenames: D3D12_BLEND_OP
req.redist: 
ms.custom: 19H1
---

# D3D12_BLEND_OP enumeration


## -description


Specifies RGB or alpha blending operations.


## -enum-fields




### -field D3D12_BLEND_OP_ADD

Add source 1 and source 2.


### -field D3D12_BLEND_OP_SUBTRACT

Subtract source 1 from source 2.


### -field D3D12_BLEND_OP_REV_SUBTRACT

Subtract source 2 from source 1.


### -field D3D12_BLEND_OP_MIN

Find the minimum of source 1 and source 2.


### -field D3D12_BLEND_OP_MAX

Find the maximum of source 1 and source 2.


## -remarks



The runtime implements RGB blending and alpha blending separately. Therefore, blend state requires separate blend operations for RGB data and alpha data. These blend operations are specified in a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc">D3D12_RENDER_TARGET_BLEND_DESC</a> structure. The two sources —source 1 and source 2— are shown in the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">blending block diagram</a>.

Blend state is used by the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger stage</a> to determine how to blend together two RGB pixel values and two alpha values. The two RGB pixel values and two alpha values are the RGB pixel value and alpha value that the pixel shader outputs and the RGB pixel value and alpha value already in the output render target. The <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend">D3D12_BLEND</a> value controls the data source that the blending stage uses to modulate values for the pixel shader, render target, or both. The <b>D3D12_BLEND_OP</b> value controls how the blending stage mathematically combines these modulated values.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
 

 

