---
UID: NE:d3d10.D3D10_FORMAT_SUPPORT
title: D3D10_FORMAT_SUPPORT (d3d10.h)
author: windows-sdk-content
description: Which resources are supported for a given format and given device (see ID3D10Device::CheckFormatSupport).
old-location: direct3d10\d3d10_format_support.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_format_support.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D10_FORMAT_SUPPORT, D3D10_FORMAT_SUPPORT enumeration [Direct3D 10], D3D10_FORMAT_SUPPORT_BLENDABLE, D3D10_FORMAT_SUPPORT_BUFFER, D3D10_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT, D3D10_FORMAT_SUPPORT_CPU_LOCKABLE, D3D10_FORMAT_SUPPORT_DEPTH_STENCIL, D3D10_FORMAT_SUPPORT_DISPLAY, D3D10_FORMAT_SUPPORT_IA_INDEX_BUFFER, D3D10_FORMAT_SUPPORT_IA_VERTEX_BUFFER, D3D10_FORMAT_SUPPORT_MIP, D3D10_FORMAT_SUPPORT_MIP_AUTOGEN, D3D10_FORMAT_SUPPORT_MULTISAMPLE_LOAD, D3D10_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET, D3D10_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE, D3D10_FORMAT_SUPPORT_RENDER_TARGET, D3D10_FORMAT_SUPPORT_SHADER_GATHER, D3D10_FORMAT_SUPPORT_SHADER_LOAD, D3D10_FORMAT_SUPPORT_SHADER_SAMPLE, D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON, D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT, D3D10_FORMAT_SUPPORT_SO_BUFFER, D3D10_FORMAT_SUPPORT_TEXTURE1D, D3D10_FORMAT_SUPPORT_TEXTURE2D, D3D10_FORMAT_SUPPORT_TEXTURE3D, D3D10_FORMAT_SUPPORT_TEXTURECUBE, d2a2c18a-93be-2cdd-860b-63f669d33214, d3d10/D3D10_FORMAT_SUPPORT, d3d10/D3D10_FORMAT_SUPPORT_BLENDABLE, d3d10/D3D10_FORMAT_SUPPORT_BUFFER, d3d10/D3D10_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT, d3d10/D3D10_FORMAT_SUPPORT_CPU_LOCKABLE, d3d10/D3D10_FORMAT_SUPPORT_DEPTH_STENCIL, d3d10/D3D10_FORMAT_SUPPORT_DISPLAY, d3d10/D3D10_FORMAT_SUPPORT_IA_INDEX_BUFFER, d3d10/D3D10_FORMAT_SUPPORT_IA_VERTEX_BUFFER, d3d10/D3D10_FORMAT_SUPPORT_MIP, d3d10/D3D10_FORMAT_SUPPORT_MIP_AUTOGEN, d3d10/D3D10_FORMAT_SUPPORT_MULTISAMPLE_LOAD, d3d10/D3D10_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET, d3d10/D3D10_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE, d3d10/D3D10_FORMAT_SUPPORT_RENDER_TARGET, d3d10/D3D10_FORMAT_SUPPORT_SHADER_GATHER, d3d10/D3D10_FORMAT_SUPPORT_SHADER_LOAD, d3d10/D3D10_FORMAT_SUPPORT_SHADER_SAMPLE, d3d10/D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON, d3d10/D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT, d3d10/D3D10_FORMAT_SUPPORT_SO_BUFFER, d3d10/D3D10_FORMAT_SUPPORT_TEXTURE1D, d3d10/D3D10_FORMAT_SUPPORT_TEXTURE2D, d3d10/D3D10_FORMAT_SUPPORT_TEXTURE3D, d3d10/D3D10_FORMAT_SUPPORT_TEXTURECUBE, direct3d10.d3d10_format_support
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_FORMAT_SUPPORT
product: Windows
targetos: Windows
req.typenames: D3D10_FORMAT_SUPPORT
req.redist: 
ms.custom: 19H1
---

# D3D10_FORMAT_SUPPORT enumeration


## -description


Which resources are supported for a given format and given device (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkformatsupport">ID3D10Device::CheckFormatSupport</a>).


## -enum-fields




### -field D3D10_FORMAT_SUPPORT_BUFFER

Buffer resources supported.


### -field D3D10_FORMAT_SUPPORT_IA_VERTEX_BUFFER

Vertex buffers supported.


### -field D3D10_FORMAT_SUPPORT_IA_INDEX_BUFFER

Index buffers supported.


### -field D3D10_FORMAT_SUPPORT_SO_BUFFER

Streaming output buffers supported.


### -field D3D10_FORMAT_SUPPORT_TEXTURE1D

1D texture resources supported.


### -field D3D10_FORMAT_SUPPORT_TEXTURE2D

2D texture resources supported.


### -field D3D10_FORMAT_SUPPORT_TEXTURE3D

3D texture resources supported.


### -field D3D10_FORMAT_SUPPORT_TEXTURECUBE

Cube texture resources supported.


### -field D3D10_FORMAT_SUPPORT_SHADER_LOAD

The intrinsic HLSL function <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load">load</a> is supported.


### -field D3D10_FORMAT_SUPPORT_SHADER_SAMPLE

The intrinsic HLSL functions <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-sample">Sample</a> supported.


### -field D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON

The intrinsic HLSL functions <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmp">SampleCmp</a> 
        and <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero">SampleCmpLevelZero</a> are supported.


### -field D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT

Reserved.


### -field D3D10_FORMAT_SUPPORT_MIP

Mipmaps are supported.


### -field D3D10_FORMAT_SUPPORT_MIP_AUTOGEN

Automatic generation of mipmaps is supported.


### -field D3D10_FORMAT_SUPPORT_RENDER_TARGET

Rendertargets are supported.


### -field D3D10_FORMAT_SUPPORT_BLENDABLE

Render target blend operations supported.


### -field D3D10_FORMAT_SUPPORT_DEPTH_STENCIL

Depth stencils supported.


### -field D3D10_FORMAT_SUPPORT_CPU_LOCKABLE

CPU locking supported.


### -field D3D10_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE

Multisampling resolution supported.


### -field D3D10_FORMAT_SUPPORT_DISPLAY

Format can be displayed on screen.


### -field D3D10_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT

Format cannot be cast to another format.


### -field D3D10_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET

Format can be used as a multisampled rendertarget.


### -field D3D10_FORMAT_SUPPORT_MULTISAMPLE_LOAD

Format can be used as a multisampled texture and read into a shader with the <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load">load</a> function.


### -field D3D10_FORMAT_SUPPORT_SHADER_GATHER

Format can be used with the <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-gather">gather</a> function. This value is available in DirectX 10.1 or higher.


### -field D3D10_FORMAT_SUPPORT_BACK_BUFFER_CAST




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
 

 

