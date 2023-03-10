---
UID: NS:d3d12shader._D3D12_SHADER_INPUT_BIND_DESC
title: D3D12_SHADER_INPUT_BIND_DESC (d3d12shader.h)
description: Describes how a shader resource is bound to a shader input. (D3D12_SHADER_INPUT_BIND_DESC)
helpviewer_keywords: ["D3D12_SHADER_INPUT_BIND_DESC","D3D12_SHADER_INPUT_BIND_DESC structure","d3d12shader/D3D12_SHADER_INPUT_BIND_DESC","direct3d12.d3d12_shader_input_bind_desc"]
old-location: direct3d12\d3d12_shader_input_bind_desc.htm
tech.root: direct3d12
ms.assetid: 4179C417-388D-4A20-8878-D074E20A706F
ms.date: 12/05/2018
ms.keywords: D3D12_SHADER_INPUT_BIND_DESC, D3D12_SHADER_INPUT_BIND_DESC structure, d3d12shader/D3D12_SHADER_INPUT_BIND_DESC, direct3d12.d3d12_shader_input_bind_desc
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
req.typenames: D3D12_SHADER_INPUT_BIND_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D12_SHADER_INPUT_BIND_DESC
 - d3d12shader/_D3D12_SHADER_INPUT_BIND_DESC
 - D3D12_SHADER_INPUT_BIND_DESC
 - d3d12shader/D3D12_SHADER_INPUT_BIND_DESC
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
 - D3D12_SHADER_INPUT_BIND_DESC
---

# D3D12_SHADER_INPUT_BIND_DESC structure


## -description

Describes how a shader resource is bound to a shader input.

## -struct-fields

### -field Name

Name of the shader resource.

### -field Type

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_input_type">D3D_SHADER_INPUT_TYPE</a>-typed value that identifies the type of data in the resource.

### -field BindPoint

Starting bind point.

### -field BindCount

Number of contiguous bind points for arrays.

### -field uFlags

A combination of <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_input_flags">D3D_SHADER_INPUT_FLAGS</a>-typed values for shader input-parameter options.

### -field ReturnType

If the input is a texture, the <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_resource_return_type">D3D_RESOURCE_RETURN_TYPE</a>-typed value that identifies the return type.

### -field Dimension

A <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_srv_dimension">D3D_SRV_DIMENSION</a>-typed value that identifies the dimensions of the bound resource.

### -field NumSamples

The number of samples for a multisampled texture; when a texture isn't multisampled, the value is set to -1 (0xFFFFFFFF).
            This is zero if the shader resource is not a recognized texture.
            If the shader resource is a structured buffer, the field contains the stride of the type in bytes.

### -field Space

The register space.

### -field uID

The range ID in the bytecode.

## -remarks

Get a shader-input-signature description by calling <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getresourcebindingdesc">ID3D12ShaderReflection::GetResourceBindingDesc</a> or <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getresourcebindingdescbyname">ID3D12ShaderReflection::GetResourceBindingDescByName</a>.

## -see-also

<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-structures">Shader Structures</a>
