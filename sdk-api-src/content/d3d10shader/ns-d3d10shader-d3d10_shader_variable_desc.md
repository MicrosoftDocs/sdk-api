---
UID: NS:d3d10shader._D3D10_SHADER_VARIABLE_DESC
title: D3D10_SHADER_VARIABLE_DESC (d3d10shader.h)
description: Describes a shader variable. (D3D10_SHADER_VARIABLE_DESC)
helpviewer_keywords: ["93d99a1e-6d9e-3991-2e0b-086cd3eee8c0","D3D10_SHADER_VARIABLE_DESC","D3D10_SHADER_VARIABLE_DESC structure [Direct3D 10]","d3d10shader/D3D10_SHADER_VARIABLE_DESC","direct3d10.d3d10_shader_variable_desc"]
old-location: direct3d10\d3d10_shader_variable_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_variable_desc.htm
ms.date: 12/05/2018
ms.keywords: 93d99a1e-6d9e-3991-2e0b-086cd3eee8c0, D3D10_SHADER_VARIABLE_DESC, D3D10_SHADER_VARIABLE_DESC structure [Direct3D 10], d3d10shader/D3D10_SHADER_VARIABLE_DESC, direct3d10.d3d10_shader_variable_desc
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
req.typenames: D3D10_SHADER_VARIABLE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_VARIABLE_DESC
 - d3d10shader/_D3D10_SHADER_VARIABLE_DESC
 - D3D10_SHADER_VARIABLE_DESC
 - d3d10shader/D3D10_SHADER_VARIABLE_DESC
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
 - D3D10_SHADER_VARIABLE_DESC
---

# D3D10_SHADER_VARIABLE_DESC structure


## -description

Describes a shader variable.

## -struct-fields

### -field Name

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The variable name.

### -field StartOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset from the start of the parent structure, to the beginning of the variable.

### -field Size

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the variable (in bytes).

### -field uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags, which identify shader-variable properties (see <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_flags">D3D10_SHADER_VARIABLE_FLAGS</a>).

### -field DefaultValue

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPVOID</a></b>

The default value for initializing the variable.

## -remarks

Get a shader-variable description using reflection, by calling <a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc">ID3D10ShaderReflectionVariable::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>
