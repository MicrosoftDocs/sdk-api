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

# D3D10_FORMAT_SUPPORT enumeration


## -description


Which resources are supported for a given format and given device (see <a href="https://msdn.microsoft.com/50b4fcbb-3c51-4027-b766-ea0590eb7766">ID3D10Device::CheckFormatSupport</a>).


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

The intrinsic HLSL function <a href="https://msdn.microsoft.com/a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8">load</a> is supported.


### -field D3D10_FORMAT_SUPPORT_SHADER_SAMPLE

The intrinsic HLSL functions <a href="https://msdn.microsoft.com/788ba4b4-8013-411f-9a19-fb9983386fa0">Sample</a> supported.


### -field D3D10_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON

The intrinsic HLSL functions <a href="https://msdn.microsoft.com/e21894c4-e8c5-4c3d-92c1-727964f8fd94">SampleCmp</a> 
        and <a href="https://msdn.microsoft.com/cecfc5e8-d293-4e0e-a3f4-b23f84843b7d">SampleCmpLevelZero</a> are supported.


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

Format can be used as a multisampled texture and read into a shader with the <a href="https://msdn.microsoft.com/a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8">load</a> function.


### -field D3D10_FORMAT_SUPPORT_SHADER_GATHER

Format can be used with the <a href="https://msdn.microsoft.com/a394d8c2-99cc-4a38-9ac9-34afc666ebe0">gather</a> function. This value is available in DirectX 10.1 or higher.


### -field D3D10_FORMAT_SUPPORT_BACK_BUFFER_CAST




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

