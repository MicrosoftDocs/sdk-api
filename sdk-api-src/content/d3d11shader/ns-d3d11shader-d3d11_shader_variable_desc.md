---
UID: NS:d3d11shader._D3D11_SHADER_VARIABLE_DESC
title: D3D11_SHADER_VARIABLE_DESC (d3d11shader.h)
description: Describes a shader variable. (D3D11_SHADER_VARIABLE_DESC)
helpviewer_keywords: ["D3D11_SHADER_VARIABLE_DESC","D3D11_SHADER_VARIABLE_DESC structure [Direct3D 11]","cfce73ab-af25-fa7f-0d0a-e49af39dc5d8","d3d11shader/D3D11_SHADER_VARIABLE_DESC","direct3d11.d3d11_shader_variable_desc"]
old-location: direct3d11\d3d11_shader_variable_desc.htm
tech.root: direct3d11
ms.assetid: b5620fea-c7d1-4db1-9bd1-991a2efa3b4c
ms.date: 12/05/2018
ms.keywords: D3D11_SHADER_VARIABLE_DESC, D3D11_SHADER_VARIABLE_DESC structure [Direct3D 11], cfce73ab-af25-fa7f-0d0a-e49af39dc5d8, d3d11shader/D3D11_SHADER_VARIABLE_DESC, direct3d11.d3d11_shader_variable_desc
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
req.typenames: D3D11_SHADER_VARIABLE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D11_SHADER_VARIABLE_DESC
 - d3d11shader/_D3D11_SHADER_VARIABLE_DESC
 - D3D11_SHADER_VARIABLE_DESC
 - d3d11shader/D3D11_SHADER_VARIABLE_DESC
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
 - D3D11_SHADER_VARIABLE_DESC
---

# D3D11_SHADER_VARIABLE_DESC structure


## -description

Describes a shader variable.

## -struct-fields

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The variable name.

### -field StartOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset from the start of the parent structure to the beginning of the variable.

### -field Size

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the variable (in bytes).

### -field uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_flags">D3D_SHADER_VARIABLE_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value identifies shader-variable properties.

### -field DefaultValue

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPVOID</a></b>

The default value for initializing the variable.

### -field StartTexture

Type: <b>UINT</b>

Offset from the start of the variable to the beginning of the texture.

### -field TextureSize

Type: <b>UINT</b>

The size of the texture, in bytes.

### -field StartSampler

Type: <b>UINT</b>

Offset from the start of the variable to the beginning of the sampler.

### -field SamplerSize

Type: <b>UINT</b>

The size of the sampler, in bytes.

## -remarks

Get a shader-variable description using reflection by calling <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc">ID3D11ShaderReflectionVariable::GetDesc</a>.
        

As of the June 2010 update, <b>DefaultValue</b> emits default values for reflection.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>
