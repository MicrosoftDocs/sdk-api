---
UID: NS:d3d10shader._D3D10_SHADER_INPUT_BIND_DESC
title: D3D10_SHADER_INPUT_BIND_DESC (d3d10shader.h)
description: Describes how a shader resource is bound to a shader input. (D3D10_SHADER_INPUT_BIND_DESC)
helpviewer_keywords: ["99c7399c-8b7c-2db1-c625-397e1a74f486","D3D10_SHADER_INPUT_BIND_DESC","D3D10_SHADER_INPUT_BIND_DESC structure [Direct3D 10]","d3d10shader/D3D10_SHADER_INPUT_BIND_DESC","direct3d10.d3d10_shader_input_bind_desc"]
old-location: direct3d10\d3d10_shader_input_bind_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_input_bind_desc.htm
ms.date: 12/05/2018
ms.keywords: 99c7399c-8b7c-2db1-c625-397e1a74f486, D3D10_SHADER_INPUT_BIND_DESC, D3D10_SHADER_INPUT_BIND_DESC structure [Direct3D 10], d3d10shader/D3D10_SHADER_INPUT_BIND_DESC, direct3d10.d3d10_shader_input_bind_desc
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
req.typenames: D3D10_SHADER_INPUT_BIND_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_INPUT_BIND_DESC
 - d3d10shader/_D3D10_SHADER_INPUT_BIND_DESC
 - D3D10_SHADER_INPUT_BIND_DESC
 - d3d10shader/D3D10_SHADER_INPUT_BIND_DESC
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
 - D3D10_SHADER_INPUT_BIND_DESC
---

# D3D10_SHADER_INPUT_BIND_DESC structure


## -description

Describes how a shader resource is bound to a shader input.

## -struct-fields

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Name of the shader resource.

### -field Type

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_input_type">D3D10_SHADER_INPUT_TYPE</a></b>

Identifies the type of data in the resource. See <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_input_type">D3D10_SHADER_INPUT_TYPE</a>.

### -field BindPoint

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Starting bind point.

### -field BindCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of contiguous bind points for arrays.

### -field uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Shader input-parameter options. See <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_input_flags">D3D10_SHADER_INPUT_FLAGS</a>.

### -field ReturnType

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_resource_return_type">D3D10_RESOURCE_RETURN_TYPE</a></b>

If the input is a texture, the return type. See <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_resource_return_type">D3D10_RESOURCE_RETURN_TYPE</a>.

### -field Dimension

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_buffer_srv">D3D10_SRV_DIMENSION</a></b>

Identifies the amount of data in the resource. See <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_buffer_srv">D3D10_SRV_DIMENSION</a>.

### -field NumSamples

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of samples for a multisampled texture; otherwise 0.

## -remarks

Get a shader-input-signature description by calling <a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflection-getresourcebindingdesc">ID3D10ShaderReflection::GetResourceBindingDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>
