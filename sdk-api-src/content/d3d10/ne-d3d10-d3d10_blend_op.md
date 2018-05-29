---
UID: NE:d3d10.D3D10_BLEND_OP
title: D3D10_BLEND_OP
author: windows-sdk-content
description: RGB or alpha blending operation.
old-location: direct3d10\d3d10_blend_op.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_blend_op.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 9bbf55a2-225d-7084-43ca-8305b06faa0d, D3D10_BLEND_OP, D3D10_BLEND_OP enumeration [Direct3D 10], D3D10_BLEND_OP_ADD, D3D10_BLEND_OP_MAX, D3D10_BLEND_OP_MIN, D3D10_BLEND_OP_REV_SUBTRACT, D3D10_BLEND_OP_SUBTRACT, d3d10/D3D10_BLEND_OP, d3d10/D3D10_BLEND_OP_ADD, d3d10/D3D10_BLEND_OP_MAX, d3d10/D3D10_BLEND_OP_MIN, d3d10/D3D10_BLEND_OP_REV_SUBTRACT, d3d10/D3D10_BLEND_OP_SUBTRACT, direct3d10.d3d10_blend_op
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: D3D10_BLEND_OP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10.h
api_name:
-	D3D10_BLEND_OP
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D3D10_BLEND_OP enumeration


## -description


RGB or alpha blending operation.


## -enum-fields




### -field D3D10_BLEND_OP_ADD

Add source 1 and source 2.


### -field D3D10_BLEND_OP_SUBTRACT

Subtract source 1 from source 2.


### -field D3D10_BLEND_OP_REV_SUBTRACT

Subtract source 2 from source 1.


### -field D3D10_BLEND_OP_MIN

Find the minimum of source 1 and source 2.


### -field D3D10_BLEND_OP_MAX

Find the maximum of source 1 and source 2.


## -remarks



The runtime implements RGB blending and alpha blending separately. Therefore, blend state requires separate blend operations for RGB data and alpha data. These blend operations are specified in a <a href="https://msdn.microsoft.com/c256dd1e-2b25-4dc5-8e49-5bf2b419b3c5">blend description</a>. The two sources — source 1 and source 2 — are shown in the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">blending block diagram</a>.

Blend state is used by the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a> to determine how to blend together two RGB pixel values and two alpha values. The two RGB pixel values and two alpha values are the RGB pixel value and alpha value that the pixel shader outputs and the RGB pixel value and alpha value already in the output render target. The <a href="https://msdn.microsoft.com/0d3a337d-3d16-4a0a-9611-b511c8fb39b4">blend option</a> controls the data source that the blending stage uses to modulate values for the pixel shader, render target, or both. The <b>blend operation</b> controls how the blending stage mathematically combines these modulated values.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

