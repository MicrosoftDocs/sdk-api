---
UID: NE:d3d10.D3D10_FORMAT_SUPPORT
title: D3D10_FORMAT_SUPPORT
author: windows-sdk-content
description: Which resources are supported for a given format and given device (see ID3D10Device::CheckFormatSupport).
old-location: direct3d10\d3d10_format_support.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_format_support.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10_FORMAT_SUPPORT, D3D10_FORMAT_SUPPORT enumeration [Direct3D 10], D3D10_FORMAT_SUPPORT_BLENDABLE, D3D10_FORMAT_SUPPORT_BUFFER, D3D10_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT, D3D10_FORMAT_SUPPORT_CPU_LOCKABLE, D3D10_FORMAT_SUPPORT_DEPTH_STENCIL, D3D10_FORMAT_SUPPORT_DISPLAY, D3D10_FORMAT_SUPPORT_IA_INDEX_BUFFER, D3D10_FORMAT_SUPPORT_IA_VERTEX_BUFFER, D3D10_FORMAT_SUPPORT_MIP, D3D10_FORMAT_SUPPORT_MIP_AUTOGEN, D3D10_FORMAT_SUPPORT_MULTISAMPLE_LOAD, D3D10_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET, D3D10_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE, D3D10_FORMAT_SUPPORT_RENDER_TARGET, D3D10_FORMAT_SUPPORT_SHADER_GATHER, D3D10_FORMAT_SUPPORT_SHADER_LOAD, D3D10_FORMAT_SUPPORT_SHADER_SAMPLE, D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON, D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT, D3D10_FORMAT_SUPPORT_SO_BUFFER, D3D10_FORMAT_SUPPORT_TEXTURE1D, D3D10_FORMAT_SUPPORT_TEXTURE2D, D3D10_FORMAT_SUPPORT_TEXTURE3D, D3D10_FORMAT_SUPPORT_TEXTURECUBE, d2a2c18a-93be-2cdd-860b-63f669d33214, d3d10/D3D10_FORMAT_SUPPORT, d3d10/D3D10_FORMAT_SUPPORT_BLENDABLE, d3d10/D3D10_FORMAT_SUPPORT_BUFFER, d3d10/D3D10_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT, d3d10/D3D10_FORMAT_SUPPORT_CPU_LOCKABLE, d3d10/D3D10_FORMAT_SUPPORT_DEPTH_STENCIL, d3d10/D3D10_FORMAT_SUPPORT_DISPLAY, d3d10/D3D10_FORMAT_SUPPORT_IA_INDEX_BUFFER, d3d10/D3D10_FORMAT_SUPPORT_IA_VERTEX_BUFFER, d3d10/D3D10_FORMAT_SUPPORT_MIP, d3d10/D3D10_FORMAT_SUPPORT_MIP_AUTOGEN, d3d10/D3D10_FORMAT_SUPPORT_MULTISAMPLE_LOAD, d3d10/D3D10_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET, d3d10/D3D10_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE, d3d10/D3D10_FORMAT_SUPPORT_RENDER_TARGET, d3d10/D3D10_FORMAT_SUPPORT_SHADER_GATHER, d3d10/D3D10_FORMAT_SUPPORT_SHADER_LOAD, d3d10/D3D10_FORMAT_SUPPORT_SHADER_SAMPLE, d3d10/D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON, d3d10/D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT, d3d10/D3D10_FORMAT_SUPPORT_SO_BUFFER, d3d10/D3D10_FORMAT_SUPPORT_TEXTURE1D, d3d10/D3D10_FORMAT_SUPPORT_TEXTURE2D, d3d10/D3D10_FORMAT_SUPPORT_TEXTURE3D, d3d10/D3D10_FORMAT_SUPPORT_TEXTURECUBE, direct3d10.d3d10_format_support
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
tech.root: 
req.typenames: D3D10_FORMAT_SUPPORT
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D3D10_FORMAT_SUPPORT enumeration


## -description


Which resources are supported for a given format and given device (see <a href="https://msdn.microsoft.com/en-us/library/Bb173536(v=VS.85).aspx">ID3D10Device::CheckFormatSupport</a>).


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

The intrinsic HLSL function <a href="https://msdn.microsoft.com/en-us/library/Bb509694(v=VS.85).aspx">load</a> is supported.


### -field D3D10_FORMAT_SUPPORT_SHADER_SAMPLE

The intrinsic HLSL functions <a href="https://msdn.microsoft.com/en-us/library/Bb509695(v=VS.85).aspx">Sample</a> supported.


### -field D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON

The intrinsic HLSL functions <a href="https://msdn.microsoft.com/en-us/library/Bb509696(v=VS.85).aspx">SampleCmp</a> 
        and <a href="https://msdn.microsoft.com/en-us/library/Bb509697(v=VS.85).aspx">SampleCmpLevelZero</a> are supported.


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

Format can be used as a multisampled texture and read into a shader with the <a href="https://msdn.microsoft.com/en-us/library/Bb509694(v=VS.85).aspx">load</a> function.


### -field D3D10_FORMAT_SUPPORT_SHADER_GATHER

Format can be used with the <a href="https://msdn.microsoft.com/en-us/library/Bb944003(v=VS.85).aspx">gather</a> function. This value is available in DirectX 10.1 or higher.


### -field D3D10_FORMAT_SUPPORT_BACK_BUFFER_CAST




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205150(v=VS.85).aspx">Core Enumerations</a>
 

 

