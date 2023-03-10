---
UID: NS:d3d11shader._D3D11_SHADER_INPUT_BIND_DESC
title: D3D11_SHADER_INPUT_BIND_DESC (d3d11shader.h)
description: Describes how a shader resource is bound to a shader input. (D3D11_SHADER_INPUT_BIND_DESC)
helpviewer_keywords: ["D3D11_SHADER_INPUT_BIND_DESC","D3D11_SHADER_INPUT_BIND_DESC structure [Direct3D 11]","b6214f45-418b-2509-b9d9-f7513efc5ba6","d3d11shader/D3D11_SHADER_INPUT_BIND_DESC","direct3d11.d3d11_shader_input_bind_desc"]
old-location: direct3d11\d3d11_shader_input_bind_desc.htm
tech.root: direct3d11
ms.assetid: 384ad8f8-0991-4cd2-bb3d-76b8338686da
ms.date: 12/05/2018
ms.keywords: D3D11_SHADER_INPUT_BIND_DESC, D3D11_SHADER_INPUT_BIND_DESC structure [Direct3D 11], b6214f45-418b-2509-b9d9-f7513efc5ba6, d3d11shader/D3D11_SHADER_INPUT_BIND_DESC, direct3d11.d3d11_shader_input_bind_desc
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
req.typenames: D3D11_SHADER_INPUT_BIND_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D11_SHADER_INPUT_BIND_DESC
 - d3d11shader/_D3D11_SHADER_INPUT_BIND_DESC
 - D3D11_SHADER_INPUT_BIND_DESC
 - d3d11shader/D3D11_SHADER_INPUT_BIND_DESC
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
 - D3D11_SHADER_INPUT_BIND_DESC
---

# D3D11_SHADER_INPUT_BIND_DESC structure


## -description

Describes how a shader resource is bound to a shader input.

## -struct-fields

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Name of the shader resource.

### -field Type

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_input_type">D3D_SHADER_INPUT_TYPE</a></b>

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_input_type">D3D_SHADER_INPUT_TYPE</a>-typed value that identifies the type of data in the resource.

### -field BindPoint

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Starting bind point.

### -field BindCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of contiguous bind points for arrays.

### -field uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_input_flags">D3D_SHADER_INPUT_FLAGS</a>-typed values for shader input-parameter options.

### -field ReturnType

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_resource_return_type">D3D_RESOURCE_RETURN_TYPE</a></b>

If the input is a texture, the <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_resource_return_type">D3D_RESOURCE_RETURN_TYPE</a>-typed value that identifies the return type.

### -field Dimension

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_srv_dimension">D3D_SRV_DIMENSION</a></b>

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_srv_dimension">D3D_SRV_DIMENSION</a>-typed value that identifies the dimensions of the bound resource.

### -field NumSamples

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of samples for a multisampled texture; when a texture isn't multisampled, the value is set to -1 (0xFFFFFFFF).

## -remarks

Get a shader-input-signature description by calling <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getresourcebindingdesc">ID3D11ShaderReflection::GetResourceBindingDesc</a> or <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getresourcebindingdescbyname">ID3D11ShaderReflection::GetResourceBindingDescByName</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>
