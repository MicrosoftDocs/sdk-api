---
UID: NS:d3d11shader._D3D11_SHADER_BUFFER_DESC
title: D3D11_SHADER_BUFFER_DESC (d3d11shader.h)
author: windows-sdk-content
description: Describes a shader constant-buffer.
old-location: direct3d11\d3d11_shader_buffer_desc.htm
tech.root: direct3d11
ms.assetid: deea8d5d-2431-4449-baa8-68a4b9b30307
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_SHADER_BUFFER_DESC, D3D11_SHADER_BUFFER_DESC structure [Direct3D 11], d3d11shader/D3D11_SHADER_BUFFER_DESC, direct3d11.d3d11_shader_buffer_desc, f067255d-ad70-0513-b346-8e4194271884
ms.topic: struct
req.header: d3d11shader.h
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
 - D3D11Shader.h
api_name:
 - D3D11_SHADER_BUFFER_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_SHADER_BUFFER_DESC
req.redist: 
---

# D3D11_SHADER_BUFFER_DESC structure


## -description


Describes a shader constant-buffer.


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the buffer.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/b21a460b-63cb-49c1-bd6c-a747df495efc">D3D_CBUFFER_TYPE</a></b>

A <a href="https://msdn.microsoft.com/b21a460b-63cb-49c1-bd6c-a747df495efc">D3D_CBUFFER_TYPE</a>-typed value that indicates the intended use of the constant data.


### -field Variables

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of unique variables.


### -field Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Buffer size (in bytes).


### -field uFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A combination of <a href="https://msdn.microsoft.com/f641b3ec-5492-4835-9cf6-e41447e4b6b6">D3D_SHADER_CBUFFER_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies properties for the shader constant-buffer.


## -remarks



Constants are supplied to shaders in a shader-constant buffer. Get the description of a shader-constant-buffer by calling <a href="https://msdn.microsoft.com/34d84751-ccce-4c18-8027-2b5477e35abc">ID3D11ShaderReflectionConstantBuffer::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

