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

# D3D12_FORMAT_SUPPORT1 enumeration


## -description


Specifies resources that are supported for a provided format.


## -enum-fields




### -field D3D12_FORMAT_SUPPORT1_NONE

No resources are supported.


### -field D3D12_FORMAT_SUPPORT1_BUFFER

Buffer resources supported.


### -field D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER

Vertex buffers supported.


### -field D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER

Index buffers supported.


### -field D3D12_FORMAT_SUPPORT1_SO_BUFFER

Streaming output buffers supported.


### -field D3D12_FORMAT_SUPPORT1_TEXTURE1D

1D texture resources supported.


### -field D3D12_FORMAT_SUPPORT1_TEXTURE2D

2D texture resources supported.


### -field D3D12_FORMAT_SUPPORT1_TEXTURE3D

3D texture resources supported.


### -field D3D12_FORMAT_SUPPORT1_TEXTURECUBE

Cube texture resources supported.


### -field D3D12_FORMAT_SUPPORT1_SHADER_LOAD

The HLSL <a href="https://msdn.microsoft.com/a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8">Load</a> function for texture objects is supported.


### -field D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE

The HLSL <a href="https://msdn.microsoft.com/788ba4b4-8013-411f-9a19-fb9983386fa0">Sample</a> function for texture objects is supported.

<div class="alert"><b>Note</b>  If the device supports the format as a resource (1D, 2D, 3D, or cube map) but doesn't support this option, the resource can still use the <a href="https://msdn.microsoft.com/788ba4b4-8013-411f-9a19-fb9983386fa0">Sample</a> method but must use only the point filtering sampler state to perform the sample.</div>
<div> </div>

### -field D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON

The HLSL <a href="https://msdn.microsoft.com/e21894c4-e8c5-4c3d-92c1-727964f8fd94">SampleCmp</a> and <a href="https://msdn.microsoft.com/cecfc5e8-d293-4e0e-a3f4-b23f84843b7d">SampleCmpLevelZero</a> functions for texture objects are supported.

<div class="alert"><b>Note</b>  Windows 8 and later might provide limited support for these functions on Direct3D <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature levels</a> 9_1, 9_2, and 9_3. For more info, see <a href="https://msdn.microsoft.com/BB8B4119-E79B-468C-A5E0-E250BF204A98">Implementing shadow buffers for Direct3D feature level 9</a>.
</div>
<div> </div>

### -field D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT

Reserved.


### -field D3D12_FORMAT_SUPPORT1_MIP

Mipmaps are supported.


### -field D3D12_FORMAT_SUPPORT1_RENDER_TARGET

Render targets are supported.


### -field D3D12_FORMAT_SUPPORT1_BLENDABLE

Blend operations supported.


### -field D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL

Depth stencils supported.


### -field D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE

Multisample antialiasing (MSAA) resolve operations are supported. For more info, see <a href="https://msdn.microsoft.com/F1D4BAD1-B08E-47D0-9D2B-41873D6B4456">ID3D12GraphicsCommandList::ResolveSubresource</a>. 


### -field D3D12_FORMAT_SUPPORT1_DISPLAY

Format can be displayed on screen.


### -field D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT

Format can't be cast to another format.


### -field D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET

Format can be used as a multi-sampled render target.


### -field D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD

Format can be used as a multi-sampled texture and read into a shader with the HLSL <a href="https://msdn.microsoft.com/a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8">Load</a> function.


### -field D3D12_FORMAT_SUPPORT1_SHADER_GATHER

Format can be used with the HLSL gather function. This value is available in DirectX 10.1 or higher.


### -field D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST

Format supports casting when the resource is a back buffer.


### -field D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW

Format can be used for an unordered access view.


### -field D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON

Format can be used with the HLSL gather with comparison function.


### -field D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT

Format can be used with the decoder output.


### -field D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT

Format can be used with the video processor output.


### -field D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT

Format can be used with the video processor input.


### -field D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER

Format can be used with the video encoder.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/6E4EB08F-0B60-4B1E-AD27-8F0AE2BD0766">D3D12_FEATURE_DATA_FORMAT_SUPPORT</a> structure. 




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/C3C1B611-714C-49DB-8034-9C9B7D6772E4">D3D12_HEAP_FLAGS</a>
 

 

