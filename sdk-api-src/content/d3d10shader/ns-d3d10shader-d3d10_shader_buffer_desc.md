---
UID: NS:d3d10shader._D3D10_SHADER_BUFFER_DESC
title: D3D10_SHADER_BUFFER_DESC (d3d10shader.h)
description: Describes a shader constant-buffer. (D3D10_SHADER_BUFFER_DESC)
helpviewer_keywords: ["149ee7ef-e8fe-d33d-b3e6-f8e1b0c4a83a","D3D10_SHADER_BUFFER_DESC","D3D10_SHADER_BUFFER_DESC structure [Direct3D 10]","d3d10shader/D3D10_SHADER_BUFFER_DESC","direct3d10.d3d10_shader_buffer_desc"]
old-location: direct3d10\d3d10_shader_buffer_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_buffer_desc.htm
ms.date: 12/05/2018
ms.keywords: 149ee7ef-e8fe-d33d-b3e6-f8e1b0c4a83a, D3D10_SHADER_BUFFER_DESC, D3D10_SHADER_BUFFER_DESC structure [Direct3D 10], d3d10shader/D3D10_SHADER_BUFFER_DESC, direct3d10.d3d10_shader_buffer_desc
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
targetos: Windows
req.typenames: D3D10_SHADER_BUFFER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_BUFFER_DESC
 - d3d10shader/_D3D10_SHADER_BUFFER_DESC
 - D3D10_SHADER_BUFFER_DESC
 - d3d10shader/D3D10_SHADER_BUFFER_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10Shader.h
api_name:
 - D3D10_SHADER_BUFFER_DESC
---

# D3D10_SHADER_BUFFER_DESC structure


## -description

Describes a shader constant-buffer.

## -struct-fields

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the buffer.

### -field Type

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb204899(v=vs.85)">D3D10_CBUFFER_TYPE</a></b>

The intended use of the constant data. See <a href="/previous-versions/windows/desktop/legacy/bb204899(v=vs.85)">D3D10_CBUFFER_TYPE</a>.

### -field Variables

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of unique variables.

### -field Size

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Buffer size (in bytes).

### -field uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Shader buffer properties. See <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_cbuffer_flags">D3D10_SHADER_CBUFFER_FLAGS</a>.

## -remarks

Constants are supplied to shaders in a shader-constant buffer. Get the description of a shader-constant-buffer by calling <a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectionconstantbuffer-getdesc">ID3D10ShaderReflectionConstantBuffer::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>
