---
UID: NE:d3d11.D3D11_BLEND_OP
title: D3D11_BLEND_OP
author: windows-sdk-content
description: RGB or alpha blending operation.
old-location: direct3d11\d3d11_blend_op.htm
tech.root: direct3d11
ms.assetid: e0a201da-0d5d-4a85-a0cb-fddd9bd2f460
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 2c289d70-b751-5cb8-a8b5-4db1d10f3c9d, D3D11_BLEND_OP, D3D11_BLEND_OP enumeration [Direct3D 11], D3D11_BLEND_OP_ADD, D3D11_BLEND_OP_MAX, D3D11_BLEND_OP_MIN, D3D11_BLEND_OP_REV_SUBTRACT, D3D11_BLEND_OP_SUBTRACT, d3d11/D3D11_BLEND_OP, d3d11/D3D11_BLEND_OP_ADD, d3d11/D3D11_BLEND_OP_MAX, d3d11/D3D11_BLEND_OP_MIN, d3d11/D3D11_BLEND_OP_REV_SUBTRACT, d3d11/D3D11_BLEND_OP_SUBTRACT, direct3d11.d3d11_blend_op
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_BLEND_OP
product: Windows
targetos: Windows
req.typenames: D3D11_BLEND_OP
req.redist: 
---

# D3D11_BLEND_OP enumeration


## -description


RGB or alpha blending operation.


## -enum-fields




### -field D3D11_BLEND_OP_ADD

Add source 1 and source 2.


### -field D3D11_BLEND_OP_SUBTRACT

Subtract source 1 from source 2.


### -field D3D11_BLEND_OP_REV_SUBTRACT

Subtract source 2 from source 1.


### -field D3D11_BLEND_OP_MIN

Find the minimum of source 1 and source 2.


### -field D3D11_BLEND_OP_MAX

Find the maximum of source 1 and source 2.


## -remarks



The runtime implements RGB blending and alpha blending separately. Therefore, blend state requires separate blend operations for RGB data and alpha data. These blend operations are specified in a <a href="https://msdn.microsoft.com/388f862c-58b0-48a8-a865-ba7568484ef5">blend description</a>. The two sources —source 1 and source 2— are shown in the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">blending block diagram</a>.

Blend state is used by the <a href="https://msdn.microsoft.com/en-us/library/Bb205120(v=VS.85).aspx">output-merger stage</a> to determine how to blend together two RGB pixel values and two alpha values. The two RGB pixel values and two alpha values are the RGB pixel value and alpha value that the pixel shader outputs and the RGB pixel value and alpha value already in the output render target. The <a href="https://msdn.microsoft.com/5fee5cfc-519e-41d9-93d4-f4f28e1826b8">blend option</a> controls the data source that the blending stage uses to modulate values for the pixel shader, render target, or both. The <b>blend operation</b> controls how the blending stage mathematically combines these modulated values.




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

