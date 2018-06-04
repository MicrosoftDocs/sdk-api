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

# D3D11_FORMAT_SUPPORT enumeration


## -description


Which resources are supported for a given format and given device (see <a href="https://msdn.microsoft.com/d5442fe8-e510-4bda-9df0-377b465cdd5e">ID3D11Device::CheckFormatSupport</a> 
    and <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a>).


## -enum-fields




### -field D3D11_FORMAT_SUPPORT_BUFFER

Buffer resources supported.


### -field D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER

Vertex buffers supported.


### -field D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER

Index buffers supported.


### -field D3D11_FORMAT_SUPPORT_SO_BUFFER

Streaming output buffers supported.


### -field D3D11_FORMAT_SUPPORT_TEXTURE1D

1D texture resources supported.


### -field D3D11_FORMAT_SUPPORT_TEXTURE2D

2D texture resources supported.


### -field D3D11_FORMAT_SUPPORT_TEXTURE3D

3D texture resources supported.


### -field D3D11_FORMAT_SUPPORT_TEXTURECUBE

Cube texture resources supported.


### -field D3D11_FORMAT_SUPPORT_SHADER_LOAD

The HLSL <a href="https://msdn.microsoft.com/a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8">Load</a> function for texture objects is supported.


### -field D3D11_FORMAT_SUPPORT_SHADER_SAMPLE

The HLSL <a href="https://msdn.microsoft.com/788ba4b4-8013-411f-9a19-fb9983386fa0">Sample</a> function for texture objects is supported.

<div class="alert"><b>Note</b>  If the device supports the format as a resource (1D, 2D, 3D, or cube map) but doesn't support this option, the resource can still use the <a href="https://msdn.microsoft.com/788ba4b4-8013-411f-9a19-fb9983386fa0">Sample</a> method but must use only the point filtering sampler state to perform the sample.</div>
<div> </div>

### -field D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON

The HLSL <a href="https://msdn.microsoft.com/e21894c4-e8c5-4c3d-92c1-727964f8fd94">SampleCmp</a> and <a href="https://msdn.microsoft.com/cecfc5e8-d293-4e0e-a3f4-b23f84843b7d">SampleCmpLevelZero</a> functions for texture objects are supported.

<div class="alert"><b>Note</b>  Windows 8 and later might provide limited support for these functions on Direct3D <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature levels</a> 9_1, 9_2, and 9_3. For more info, see <a href="https://msdn.microsoft.com/BB8B4119-E79B-468C-A5E0-E250BF204A98">Implementing shadow buffers for Direct3D feature level 9</a>.
</div>
<div> </div>

### -field D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT

Reserved.


### -field D3D11_FORMAT_SUPPORT_MIP

Mipmaps are supported.


### -field D3D11_FORMAT_SUPPORT_MIP_AUTOGEN

Automatic generation of mipmaps is supported.


### -field D3D11_FORMAT_SUPPORT_RENDER_TARGET

Render targets are supported.


### -field D3D11_FORMAT_SUPPORT_BLENDABLE

Blend operations supported.


### -field D3D11_FORMAT_SUPPORT_DEPTH_STENCIL

Depth stencils supported.


### -field D3D11_FORMAT_SUPPORT_CPU_LOCKABLE

CPU locking supported.


### -field D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE

Multisample antialiasing (MSAA) resolve operations are supported. For more info, see <a href="https://msdn.microsoft.com/7b4d6180-e3bf-475a-9865-592cda6e9f4a">ID3D11DeviceContex::ResolveSubresource</a>. 


### -field D3D11_FORMAT_SUPPORT_DISPLAY

Format can be displayed on screen.


### -field D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT

Format cannot be cast to another format.


### -field D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET

Format can be used as a multisampled rendertarget.


### -field D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD

Format can be used as a multisampled texture and read into a shader with the HLSL load function.


### -field D3D11_FORMAT_SUPPORT_SHADER_GATHER

Format can be used with the HLSL gather function. This value is available in DirectX 10.1 or higher.


### -field D3D11_FORMAT_SUPPORT_BACK_BUFFER_CAST

Format supports casting when the resource is a back buffer.


### -field D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW

Format can be used for an unordered access view.


### -field D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON

Format can be used with the HLSL gather with comparison function.


### -field D3D11_FORMAT_SUPPORT_DECODER_OUTPUT

Format can be used with the decoder output.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


### -field D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT

Format can be used with the video processor output.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


### -field D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT

Format can be used with the video processor input.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


### -field D3D11_FORMAT_SUPPORT_VIDEO_ENCODER

Format can be used with the video encoder.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

