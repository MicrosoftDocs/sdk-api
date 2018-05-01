---
UID: NE:d3d12.D3D12_FORMAT_SUPPORT1
title: D3D12_FORMAT_SUPPORT1
author: windows-driver-content
description: Specifies resources that are supported for a provided format.
old-location: direct3d12\d3d12_format_support1.htm
old-project: direct3d12
ms.assetid: D987B228-4BC9-4A07-96A0-A518F8F52B06
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: D3D12_FORMAT_SUPPORT1, D3D12_FORMAT_SUPPORT1 enumeration, D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST, D3D12_FORMAT_SUPPORT1_BLENDABLE, D3D12_FORMAT_SUPPORT1_BUFFER, D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT, D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT, D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL, D3D12_FORMAT_SUPPORT1_DISPLAY, D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER, D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER, D3D12_FORMAT_SUPPORT1_MIP, D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD, D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET, D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT1_RENDER_TARGET, D3D12_FORMAT_SUPPORT1_SHADER_GATHER, D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON, D3D12_FORMAT_SUPPORT1_SHADER_LOAD, D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE, D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON, D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT, D3D12_FORMAT_SUPPORT1_SO_BUFFER, D3D12_FORMAT_SUPPORT1_TEXTURE1D, D3D12_FORMAT_SUPPORT1_TEXTURE2D, D3D12_FORMAT_SUPPORT1_TEXTURE3D, D3D12_FORMAT_SUPPORT1_TEXTURECUBE, D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW, D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER, D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT, D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT, d3d12/D3D12_FORMAT_SUPPORT1, d3d12/D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST, d3d12/D3D12_FORMAT_SUPPORT1_BLENDABLE, d3d12/D3D12_FORMAT_SUPPORT1_BUFFER, d3d12/D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT, d3d12/D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT, d3d12/D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL, d3d12/D3D12_FORMAT_SUPPORT1_DISPLAY, d3d12/D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER, d3d12/D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER, d3d12/D3D12_FORMAT_SUPPORT1_MIP, d3d12/D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD, d3d12/D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET, d3d12/D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE, d3d12/D3D12_FORMAT_SUPPORT1_NONE, d3d12/D3D12_FORMAT_SUPPORT1_RENDER_TARGET, d3d12/D3D12_FORMAT_SUPPORT1_SHADER_GATHER, d3d12/D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON, d3d12/D3D12_FORMAT_SUPPORT1_SHADER_LOAD, d3d12/D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE, d3d12/D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON, d3d12/D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT, d3d12/D3D12_FORMAT_SUPPORT1_SO_BUFFER, d3d12/D3D12_FORMAT_SUPPORT1_TEXTURE1D, d3d12/D3D12_FORMAT_SUPPORT1_TEXTURE2D, d3d12/D3D12_FORMAT_SUPPORT1_TEXTURE3D, d3d12/D3D12_FORMAT_SUPPORT1_TEXTURECUBE, d3d12/D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW, d3d12/D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER, d3d12/D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT, d3d12/D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT, direct3d12.d3d12_format_support1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3D12_FORMAT_SUPPORT1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_FORMAT_SUPPORT1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

