---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_SCOPEVAR_INFO
title: D3D10_SHADER_DEBUG_SCOPEVAR_INFO (d3d10_1shader.h)
description: Describes a shader scope variable.
helpviewer_keywords: ["90b648c2-0ae3-a5f5-05de-ba4f5d6c85d1","D3D10_SHADER_DEBUG_SCOPEVAR_INFO","D3D10_SHADER_DEBUG_SCOPEVAR_INFO structure [Direct3D 10]","d3d10_1shader/D3D10_SHADER_DEBUG_SCOPEVAR_INFO","direct3d10.d3d10_shader_debug_scopevar_info"]
old-location: direct3d10\d3d10_shader_debug_scopevar_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_scopevar_info.htm
ms.date: 12/05/2018
ms.keywords: 90b648c2-0ae3-a5f5-05de-ba4f5d6c85d1, D3D10_SHADER_DEBUG_SCOPEVAR_INFO, D3D10_SHADER_DEBUG_SCOPEVAR_INFO structure [Direct3D 10], d3d10_1shader/D3D10_SHADER_DEBUG_SCOPEVAR_INFO, direct3d10.d3d10_shader_debug_scopevar_info
req.header: d3d10_1shader.h
req.include-header: D3D10Shader.h
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
req.typenames: D3D10_SHADER_DEBUG_SCOPEVAR_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_SCOPEVAR_INFO
 - d3d10_1shader/_D3D10_SHADER_DEBUG_SCOPEVAR_INFO
 - D3D10_SHADER_DEBUG_SCOPEVAR_INFO
 - d3d10_1shader/D3D10_SHADER_DEBUG_SCOPEVAR_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1shader.h
api_name:
 - D3D10_SHADER_DEBUG_SCOPEVAR_INFO
---

# D3D10_SHADER_DEBUG_SCOPEVAR_INFO structure


## -description

Describes a shader scope variable.

## -struct-fields

### -field TokenId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into variable token.

### -field VarType

Type: <b><a href="/windows/win32/api/d3d10_1shader/ne-d3d10_1shader-d3d10_shader_debug_vartype">D3D10_SHADER_DEBUG_VARTYPE</a></b>

Indicates whether this is a variable or function.

### -field Class

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class">D3D10_SHADER_VARIABLE_CLASS</a></b>

Indicates the variable class.

### -field Rows

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of row for matrices.

### -field Columns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of columns for vectors or matrices.

### -field StructMemberScope

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Gives a scope to look up struct members.  This member will be -1 if <b>D3D10_SHADER_DEBUG_SCOPEVAR_INFO</b> does not refer to a struct.

### -field uArrayIndices

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of array indices. For example a three dimensional array would have a value of 3 for <b>uArrayIndices</b>.

### -field ArrayElements

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to an array of UINT values <b>uArrayIndices</b> long.  The array contains the maximum value for each index. For example an array a[3][2][1] would have the values {3,2,1} at the offset pointed to by <b>ArrayElements</b>.

### -field ArrayStrides

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to an array of UINT values <b>uArrayIndices</b> long.  The array contains the stride for each array index.  For example an array a[3][2][1] would have the values {2,1,1} at the offset pointed to by <b>ArrayStrides</b>.

### -field uVariables

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of variables.

### -field uFirstVariable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first variable, later variables are offsets from this one.

## -remarks

The <b>D3D10_SHADER_DEBUG_SCOPEVAR_INFO</b> structure is used with the <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_info">D3D10_SHADER_DEBUG_INFO</a> structure.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>