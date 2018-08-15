---
UID: NS:d3d10effect._D3D10_STATE_BLOCK_MASK
title: "_D3D10_STATE_BLOCK_MASK"
author: windows-sdk-content
description: Indicates the device state.
old-location: direct3d10\d3d10_state_block_mask.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_state_block_mask.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10_STATE_BLOCK_MASK, D3D10_STATE_BLOCK_MASK structure [Direct3D 10], _D3D10_STATE_BLOCK_MASK, bf81f800-b1fd-0774-8da5-ae9bd9fc43d4, d3d10effect/D3D10_STATE_BLOCK_MASK, direct3d10.d3d10_state_block_mask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10effect.h
req.include-header: D3D10.h
req.redist: 
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
req.typenames: D3D10_STATE_BLOCK_MASK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10effect.h
api_name:
 - D3D10_STATE_BLOCK_MASK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_STATE_BLOCK_MASK structure


## -description


Indicates the device state.


## -struct-fields




### -field VS

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the vertex shader state.


### -field VSSamplers

 


### -field VSShaderResources

 


### -field VSConstantBuffers

 


### -field GS

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the geometry shader state.


### -field GSSamplers

 


### -field GSShaderResources

 


### -field GSConstantBuffers

 


### -field PS

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the pixel shader state.


### -field PSSamplers

 


### -field PSShaderResources

 


### -field PSConstantBuffers

 


### -field IAVertexBuffers

 


### -field IAIndexBuffer

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the index buffer state.


### -field IAInputLayout

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the input layout state.


### -field IAPrimitiveTopology

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the primitive topology state.


### -field OMRenderTargets

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the render targets states.


### -field OMDepthStencilState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the depth-stencil state.


### -field OMBlendState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the blend state.


### -field RSViewports

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the viewports states.


### -field RSScissorRects

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the scissor rectangles states.


### -field RSRasterizerState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the rasterizer state.


### -field SOBuffers

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the stream-out buffers states.


### -field Predication

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Boolean value indicating whether to save the predication state.


#### - GSConstantBuffers[D3D10_BYTES_FROM_BITS(D3D10_COMMONSHADER_CONSTANT_BUFFER_SLOT_COUNT)]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Array of geometry-shader constant buffers. The array is a multi-byte bitmask where each bit represents one buffer slot.


#### - GSSamplers[D3D10_BYTES_FROM_BITS(D3D10_COMMONSHADER_SAMPLER_SLOT_COUNT)]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Array of geometry-shader samplers. The array is a multi-byte bitmask where each bit represents one sampler slot.


#### - GSShaderResources[D3D10_BYTES_FROM_BITS(D3D10_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Array of geometry-shader resources. The array is a multi-byte bitmask where each bit represents one resource slot.


#### - IAVertexBuffers[D3D10_BYTES_FROM_BITS(D3D10_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Array of vertex buffers. The array is a multi-byte bitmask where each bit represents one resource slot.


#### - PSConstantBuffers[D3D10_BYTES_FROM_BITS(D3D10_COMMONSHADER_CONSTANT_BUFFER_SLOT_COUNT)]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Array of pixel-shader constant buffers. The array is a multi-byte bitmask where each bit represents one constant buffer slot.


#### - PSSamplers[D3D10_BYTES_FROM_BITS(D3D10_COMMONSHADER_SAMPLER_SLOT_COUNT)]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Array of pixel-shader samplers. The array is a multi-byte bitmask where each bit represents one sampler slot.


#### - PSShaderResources[D3D10_BYTES_FROM_BITS(D3D10_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Array of pixel-shader resources. The array is a multi-byte bitmask where each bit represents one resource slot.


#### - VSConstantBuffers[D3D10_BYTES_FROM_BITS(D3D10_COMMONSHADER_CONSTANT_BUFFER_SLOT_COUNT)]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Array of vertex-shader constant buffers. The array is a multi-byte bitmask where each bit represents one constant buffer slot.


#### - VSSamplers[D3D10_BYTES_FROM_BITS(D3D10_COMMONSHADER_SAMPLER_SLOT_COUNT)]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Array of vertex-shader samplers.  The array is a multi-byte bitmask where each bit represents one sampler slot.


#### - VSShaderResources[D3D10_BYTES_FROM_BITS(D3D10_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Array of vertex-shader resources. The array is a multi-byte bitmask where each bit represents one resource slot.


## -remarks



A state-block mask indicates the device states that a pass or a technique changes.  The <a href="https://msdn.microsoft.com/85e4a56d-016b-42e3-9ec8-b279fd4bd95b">D3D10StateBlockMaskEnableCapture</a> function 
      provides a convenient way of setting a range of bitmasks for the array members of <b>D3D10_STATE_BLOCK_MASK</b>.




## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

