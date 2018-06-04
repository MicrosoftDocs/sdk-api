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



The runtime implements RGB blending and alpha blending separately. Therefore, blend state requires separate blend operations for RGB data and alpha data. These blend operations are specified in a <a href="https://msdn.microsoft.com/388f862c-58b0-48a8-a865-ba7568484ef5">blend description</a>. The two sources —source 1 and source 2— are shown in the <a href="d3d10_graphics_programming_guide_output_merger_stage.htm">blending block diagram</a>.

Blend state is used by the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a> to determine how to blend together two RGB pixel values and two alpha values. The two RGB pixel values and two alpha values are the RGB pixel value and alpha value that the pixel shader outputs and the RGB pixel value and alpha value already in the output render target. The <a href="https://msdn.microsoft.com/5fee5cfc-519e-41d9-93d4-f4f28e1826b8">blend option</a> controls the data source that the blending stage uses to modulate values for the pixel shader, render target, or both. The <b>blend operation</b> controls how the blending stage mathematically combines these modulated values.




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

