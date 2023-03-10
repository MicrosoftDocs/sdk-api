---
UID: NS:d3d10shader._D3D10_SHADER_TYPE_DESC
title: D3D10_SHADER_TYPE_DESC (d3d10shader.h)
description: Describes a shader-variable type. (D3D10_SHADER_TYPE_DESC)
helpviewer_keywords: ["D3D10_SHADER_TYPE_DESC","D3D10_SHADER_TYPE_DESC structure [Direct3D 10]","b18f1523-7db4-ff5b-d9ab-04f0e773c99b","d3d10shader/D3D10_SHADER_TYPE_DESC","direct3d10.d3d10_shader_type_desc"]
old-location: direct3d10\d3d10_shader_type_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_type_desc.htm
ms.date: 12/05/2018
ms.keywords: D3D10_SHADER_TYPE_DESC, D3D10_SHADER_TYPE_DESC structure [Direct3D 10], b18f1523-7db4-ff5b-d9ab-04f0e773c99b, d3d10shader/D3D10_SHADER_TYPE_DESC, direct3d10.d3d10_shader_type_desc
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
req.typenames: D3D10_SHADER_TYPE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_TYPE_DESC
 - d3d10shader/_D3D10_SHADER_TYPE_DESC
 - D3D10_SHADER_TYPE_DESC
 - d3d10shader/D3D10_SHADER_TYPE_DESC
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
 - D3D10_SHADER_TYPE_DESC
---

# D3D10_SHADER_TYPE_DESC structure


## -description

Describes a shader-variable type.

## -struct-fields

### -field Class

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class">D3D10_SHADER_VARIABLE_CLASS</a></b>

Identifies the variable class as one of scalar, vector, matrix or object. See <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class">D3D10_SHADER_VARIABLE_CLASS</a>.

### -field Type

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type">D3D10_SHADER_VARIABLE_TYPE</a></b>

The variable type. See <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type">D3D10_SHADER_VARIABLE_TYPE</a>.

### -field Rows

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of rows in a matrix. Otherwise a numeric type returns 1, any other type returns 0.

### -field Columns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of columns in a matrix. Otherwise a numeric type returns 1, any other type returns 0.

### -field Elements

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of elements in an array; otherwise 0.

### -field Members

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of members in the structure; otherwise 0.

### -field Offset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset, in bytes, between the start of the parent structure and this variable.

## -remarks

Get a shader-variable-type description by calling <a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectiontype-getdesc">ID3D10ShaderReflectionType::GetDesc</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>
