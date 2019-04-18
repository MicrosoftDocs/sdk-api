---
UID: NS:d3d10shader._D3D10_SHADER_BUFFER_DESC
title: D3D10_SHADER_BUFFER_DESC (d3d10shader.h)
author: windows-sdk-content
description: Describes a shader constant-buffer.
old-location: direct3d10\d3d10_shader_buffer_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_buffer_desc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 149ee7ef-e8fe-d33d-b3e6-f8e1b0c4a83a, D3D10_SHADER_BUFFER_DESC, D3D10_SHADER_BUFFER_DESC structure [Direct3D 10], d3d10shader/D3D10_SHADER_BUFFER_DESC, direct3d10.d3d10_shader_buffer_desc
ms.topic: struct
req.header: d3d10shader.h
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
 - D3D10Shader.h
api_name:
 - D3D10_SHADER_BUFFER_DESC
product: Windows
targetos: Windows
req.typenames: D3D10_SHADER_BUFFER_DESC
req.redist: 
ms.custom: 19H1
---

# D3D10_SHADER_BUFFER_DESC structure


## -description


Describes a shader constant-buffer.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the buffer.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb204899(v=VS.85).aspx">D3D10_CBUFFER_TYPE</a></b>

The intended use of the constant data. See <a href="https://msdn.microsoft.com/en-us/library/Bb204899(v=VS.85).aspx">D3D10_CBUFFER_TYPE</a>.


### -field Variables

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of unique variables.


### -field Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Buffer size (in bytes).


### -field uFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Shader buffer properties. See <a href="https://msdn.microsoft.com/en-us/library/Bb172418(v=VS.85).aspx">D3D10_SHADER_CBUFFER_FLAGS</a>.


## -remarks



Constants are supplied to shaders in a shader-constant buffer. Get the description of a shader-constant-buffer by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173837(v=VS.85).aspx">ID3D10ShaderReflectionConstantBuffer::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205159(v=VS.85).aspx">Shader Structures</a>
 

 

