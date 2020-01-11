---
UID: NE:d3d11.D3D11_FORMAT_SUPPORT
title: D3D11_FORMAT_SUPPORT (d3d11.h)
description: Which resources are supported for a given format and given device (see ID3D11Device::CheckFormatSupport and ID3D11Device::CheckFeatureSupport).
old-location: direct3d11\d3d11_format_support.htm
tech.root: direct3d11
ms.assetid: 8c7f62fd-e0fe-4f4d-8c88-ccf1372842f9
ms.date: 12/05/2018
ms.keywords: 57619337-37ad-ca57-755b-df101a510d79, D3D11_FORMAT_SUPPORT, D3D11_FORMAT_SUPPORT enumeration [Direct3D 11], D3D11_FORMAT_SUPPORT_BACK_BUFFER_CAST, D3D11_FORMAT_SUPPORT_BLENDABLE, D3D11_FORMAT_SUPPORT_BUFFER, D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT, D3D11_FORMAT_SUPPORT_CPU_LOCKABLE, D3D11_FORMAT_SUPPORT_DECODER_OUTPUT, D3D11_FORMAT_SUPPORT_DEPTH_STENCIL, D3D11_FORMAT_SUPPORT_DISPLAY, D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER, D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER, D3D11_FORMAT_SUPPORT_MIP, D3D11_FORMAT_SUPPORT_MIP_AUTOGEN, D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD, D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET, D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE, D3D11_FORMAT_SUPPORT_RENDER_TARGET, D3D11_FORMAT_SUPPORT_SHADER_GATHER, D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON, D3D11_FORMAT_SUPPORT_SHADER_LOAD, D3D11_FORMAT_SUPPORT_SHADER_SAMPLE, D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON, D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT, D3D11_FORMAT_SUPPORT_SO_BUFFER, D3D11_FORMAT_SUPPORT_TEXTURE1D, D3D11_FORMAT_SUPPORT_TEXTURE2D, D3D11_FORMAT_SUPPORT_TEXTURE3D, D3D11_FORMAT_SUPPORT_TEXTURECUBE, D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW, D3D11_FORMAT_SUPPORT_VIDEO_ENCODER, D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT, D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT, d3d11/D3D11_FORMAT_SUPPORT, d3d11/D3D11_FORMAT_SUPPORT_BACK_BUFFER_CAST, d3d11/D3D11_FORMAT_SUPPORT_BLENDABLE, d3d11/D3D11_FORMAT_SUPPORT_BUFFER, d3d11/D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT, d3d11/D3D11_FORMAT_SUPPORT_CPU_LOCKABLE, d3d11/D3D11_FORMAT_SUPPORT_DECODER_OUTPUT, d3d11/D3D11_FORMAT_SUPPORT_DEPTH_STENCIL, d3d11/D3D11_FORMAT_SUPPORT_DISPLAY, d3d11/D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER, d3d11/D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER, d3d11/D3D11_FORMAT_SUPPORT_MIP, d3d11/D3D11_FORMAT_SUPPORT_MIP_AUTOGEN, d3d11/D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD, d3d11/D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET, d3d11/D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE, d3d11/D3D11_FORMAT_SUPPORT_RENDER_TARGET, d3d11/D3D11_FORMAT_SUPPORT_SHADER_GATHER, d3d11/D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON, d3d11/D3D11_FORMAT_SUPPORT_SHADER_LOAD, d3d11/D3D11_FORMAT_SUPPORT_SHADER_SAMPLE, d3d11/D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON, d3d11/D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT, d3d11/D3D11_FORMAT_SUPPORT_SO_BUFFER, d3d11/D3D11_FORMAT_SUPPORT_TEXTURE1D, d3d11/D3D11_FORMAT_SUPPORT_TEXTURE2D, d3d11/D3D11_FORMAT_SUPPORT_TEXTURE3D, d3d11/D3D11_FORMAT_SUPPORT_TEXTURECUBE, d3d11/D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW, d3d11/D3D11_FORMAT_SUPPORT_VIDEO_ENCODER, d3d11/D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT, d3d11/D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT, direct3d11.d3d11_format_support
f1_keywords:
- d3d11/D3D11_FORMAT_SUPPORT
dev_langs:
- c++
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
- D3D11_FORMAT_SUPPORT
targetos: Windows
req.typenames: D3D11_FORMAT_SUPPORT
req.redist: 
ms.custom: 19H1
---

# D3D11_FORMAT_SUPPORT enumeration


## -description


Which resources are supported for a given format and given device (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport">ID3D11Device::CheckFormatSupport</a> 
    and <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">ID3D11Device::CheckFeatureSupport</a>).


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

The HLSL <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load">Load</a> function for texture objects is supported.


### -field D3D11_FORMAT_SUPPORT_SHADER_SAMPLE

The HLSL <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample">Sample</a> function for texture objects is supported.

<div class="alert"><b>Note</b>  If the device supports the format as a resource (1D, 2D, 3D, or cube map) but doesn't support this option, the resource can still use the <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample">Sample</a> method but must use only the point filtering sampler state to perform the sample.</div>
<div> </div>

### -field D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON

The HLSL <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmp">SampleCmp</a> and <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero">SampleCmpLevelZero</a> functions for texture objects are supported.

<div class="alert"><b>Note</b>  Windows 8 and later might provide limited support for these functions on Direct3D <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature levels</a> 9_1, 9_2, and 9_3. For more info, see <a href="https://docs.microsoft.com/previous-versions/windows/apps/jj262110(v=win.10)">Implementing shadow buffers for Direct3D feature level 9</a>.
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

Multisample antialiasing (MSAA) resolve operations are supported. For more info, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-resolvesubresource">ID3D11DeviceContex::ResolveSubresource</a>. 


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




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
 

 

