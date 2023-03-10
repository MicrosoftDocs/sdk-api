---
UID: NS:d3d11shader._D3D11_SHADER_BUFFER_DESC
title: D3D11_SHADER_BUFFER_DESC (d3d11shader.h)
description: Describes a shader constant-buffer. (D3D11_SHADER_BUFFER_DESC)
helpviewer_keywords: ["D3D11_SHADER_BUFFER_DESC","D3D11_SHADER_BUFFER_DESC structure [Direct3D 11]","d3d11shader/D3D11_SHADER_BUFFER_DESC","direct3d11.d3d11_shader_buffer_desc","f067255d-ad70-0513-b346-8e4194271884"]
old-location: direct3d11\d3d11_shader_buffer_desc.htm
tech.root: direct3d11
ms.assetid: deea8d5d-2431-4449-baa8-68a4b9b30307
ms.date: 12/05/2018
ms.keywords: D3D11_SHADER_BUFFER_DESC, D3D11_SHADER_BUFFER_DESC structure [Direct3D 11], d3d11shader/D3D11_SHADER_BUFFER_DESC, direct3d11.d3d11_shader_buffer_desc, f067255d-ad70-0513-b346-8e4194271884
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
targetos: Windows
req.typenames: D3D11_SHADER_BUFFER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D11_SHADER_BUFFER_DESC
 - d3d11shader/_D3D11_SHADER_BUFFER_DESC
 - D3D11_SHADER_BUFFER_DESC
 - d3d11shader/D3D11_SHADER_BUFFER_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11Shader.h
api_name:
 - D3D11_SHADER_BUFFER_DESC
---

# D3D11_SHADER_BUFFER_DESC structure


## -description

Describes a shader constant-buffer.

## -struct-fields

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the buffer.

### -field Type

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_cbuffer_type">D3D_CBUFFER_TYPE</a></b>

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_cbuffer_type">D3D_CBUFFER_TYPE</a>-typed value that indicates the intended use of the constant data.

### -field Variables

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of unique variables.

### -field Size

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Buffer size (in bytes).

### -field uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_cbuffer_flags">D3D_SHADER_CBUFFER_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies properties for the shader constant-buffer.

## -remarks

Constants are supplied to shaders in a shader-constant buffer. Get the description of a shader-constant-buffer by calling <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionconstantbuffer-getdesc">ID3D11ShaderReflectionConstantBuffer::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>
