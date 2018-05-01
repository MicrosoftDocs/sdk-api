---
UID: NS:d3d10shader._D3D10_SHADER_BUFFER_DESC
title: "_D3D10_SHADER_BUFFER_DESC"
author: windows-driver-content
description: Describes a shader constant-buffer.
old-location: direct3d10\d3d10_shader_buffer_desc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_buffer_desc.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 149ee7ef-e8fe-d33d-b3e6-f8e1b0c4a83a, D3D10_SHADER_BUFFER_DESC, D3D10_SHADER_BUFFER_DESC structure [Direct3D 10], _D3D10_SHADER_BUFFER_DESC, d3d10shader/D3D10_SHADER_BUFFER_DESC, direct3d10.d3d10_shader_buffer_desc
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D10_SHADER_BUFFER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10Shader.h
api_name:
-	D3D10_SHADER_BUFFER_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3D10_SHADER_BUFFER_DESC structure


## -description


Describes a shader constant-buffer.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the buffer.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/1aba3e72-8ebe-48e7-9af6-04bf0469e879">D3D10_CBUFFER_TYPE</a></b>

The intended use of the constant data. See <a href="https://msdn.microsoft.com/1aba3e72-8ebe-48e7-9af6-04bf0469e879">D3D10_CBUFFER_TYPE</a>.


### -field Variables

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of unique variables.


### -field Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Buffer size (in bytes).


### -field uFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Shader buffer properties. See <a href="https://msdn.microsoft.com/7dde4388-6f65-4533-86d0-0b6f5619ccd8">D3D10_SHADER_CBUFFER_FLAGS</a>.


## -remarks



Constants are supplied to shaders in a shader-constant buffer. Get the description of a shader-constant-buffer by calling <a href="https://msdn.microsoft.com/30380e1d-4f89-4008-9e3d-112de4a61fb2">ID3D10ShaderReflectionConstantBuffer::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

