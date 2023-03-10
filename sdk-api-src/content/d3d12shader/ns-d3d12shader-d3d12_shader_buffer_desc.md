---
UID: NS:d3d12shader._D3D12_SHADER_BUFFER_DESC
title: D3D12_SHADER_BUFFER_DESC (d3d12shader.h)
description: Describes a shader constant-buffer. (D3D12_SHADER_BUFFER_DESC)
helpviewer_keywords: ["D3D12_SHADER_BUFFER_DESC","D3D12_SHADER_BUFFER_DESC structure","d3d12shader/D3D12_SHADER_BUFFER_DESC","direct3d12.d3d12_shader_buffer_desc"]
old-location: direct3d12\d3d12_shader_buffer_desc.htm
tech.root: direct3d12
ms.assetid: 03F36467-9841-4385-9962-D7ADB4D79C6C
ms.date: 12/05/2018
ms.keywords: D3D12_SHADER_BUFFER_DESC, D3D12_SHADER_BUFFER_DESC structure, d3d12shader/D3D12_SHADER_BUFFER_DESC, direct3d12.d3d12_shader_buffer_desc
req.header: d3d12shader.h
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
req.typenames: D3D12_SHADER_BUFFER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D12_SHADER_BUFFER_DESC
 - d3d12shader/_D3D12_SHADER_BUFFER_DESC
 - D3D12_SHADER_BUFFER_DESC
 - d3d12shader/D3D12_SHADER_BUFFER_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12shader.h
api_name:
 - D3D12_SHADER_BUFFER_DESC
---

# D3D12_SHADER_BUFFER_DESC structure


## -description

Describes a shader constant-buffer.

## -struct-fields

### -field Name

The name of the buffer.

### -field Type

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_cbuffer_type">D3D_CBUFFER_TYPE</a>-typed value that indicates the intended use of the constant data.

### -field Variables

The number of unique variables.

### -field Size

The size of the buffer, in bytes.

### -field uFlags

A combination of <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_cbuffer_flags">D3D_SHADER_CBUFFER_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies properties for the shader constant-buffer.

## -remarks

Constants are supplied to shaders in a shader-constant buffer. Get the description of a shader-constant-buffer by calling <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflectionconstantbuffer-getdesc">ID3D12ShaderReflectionConstantBuffer::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-structures">Shader Structures</a>
