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

# _D3D10_DEVICE_STATE_TYPES enumeration


## -description


Effect device-state types.


## -enum-fields




### -field D3D10_DST_SO_BUFFERS

Stream-output buffer.


### -field D3D10_DST_OM_RENDER_TARGETS

Render target.


### -field D3D10_DST_OM_DEPTH_STENCIL_STATE

Depth-stencil state.


### -field D3D10_DST_OM_BLEND_STATE

Blend state.


### -field D3D10_DST_VS

Vertex shader.


### -field D3D10_DST_VS_SAMPLERS

Vertex shader sampler.


### -field D3D10_DST_VS_SHADER_RESOURCES

Vertex shader resource.


### -field D3D10_DST_VS_CONSTANT_BUFFERS

Vertex shader constant buffer.


### -field D3D10_DST_GS

Geometry shader.


### -field D3D10_DST_GS_SAMPLERS

Geometry shader sampler.


### -field D3D10_DST_GS_SHADER_RESOURCES

Geometry shader resource.


### -field D3D10_DST_GS_CONSTANT_BUFFERS

Geometry shader constant buffer.


### -field D3D10_DST_PS

Pixel shader.


### -field D3D10_DST_PS_SAMPLERS

Pixel shader sampler.


### -field D3D10_DST_PS_SHADER_RESOURCES

Pixel shader resource.


### -field D3D10_DST_PS_CONSTANT_BUFFERS

Pixel shader constant buffer.


### -field D3D10_DST_IA_VERTEX_BUFFERS

Input-assembler vertex buffer.


### -field D3D10_DST_IA_INDEX_BUFFER

Input-assembler index buffer.


### -field D3D10_DST_IA_INPUT_LAYOUT

Input-assembler input layout.


### -field D3D10_DST_IA_PRIMITIVE_TOPOLOGY

Input-assembler primitive topology.


### -field D3D10_DST_RS_VIEWPORTS

Viewport.


### -field D3D10_DST_RS_SCISSOR_RECTS

Scissor rectangle.


### -field D3D10_DST_RS_RASTERIZER_STATE

Rasterizer state.


### -field D3D10_DST_PREDICATION

Predication state.


## -remarks



This enumeration is used by <a href="https://msdn.microsoft.com/ef68ea4a-5648-426b-8e45-ea801ade13f2">D3D10StateBlockMaskDisableCapture</a>, <a href="https://msdn.microsoft.com/85e4a56d-016b-42e3-9ec8-b279fd4bd95b">D3D10StateBlockMaskEnableCapture</a>, and <a href="https://msdn.microsoft.com/01bf6437-71f5-455a-8028-1df203b33759">D3D10StateBlockMaskGetSetting</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

