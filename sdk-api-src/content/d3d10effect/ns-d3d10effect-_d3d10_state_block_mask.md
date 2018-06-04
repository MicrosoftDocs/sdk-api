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
 

 

