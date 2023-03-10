---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_VAR_INFO
title: D3D10_SHADER_DEBUG_VAR_INFO (d3d10_1shader.h)
description: Represents information about a shader source variable.
helpviewer_keywords: ["0c0984a6-cb8d-ef1f-dfe5-bbc4ed81714f","D3D10_SHADER_DEBUG_VAR_INFO","D3D10_SHADER_DEBUG_VAR_INFO structure [Direct3D 10]","d3d10_1shader/D3D10_SHADER_DEBUG_VAR_INFO","direct3d10.d3d10_shader_debug_var_info"]
old-location: direct3d10\d3d10_shader_debug_var_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_var_info.htm
ms.date: 12/05/2018
ms.keywords: 0c0984a6-cb8d-ef1f-dfe5-bbc4ed81714f, D3D10_SHADER_DEBUG_VAR_INFO, D3D10_SHADER_DEBUG_VAR_INFO structure [Direct3D 10], d3d10_1shader/D3D10_SHADER_DEBUG_VAR_INFO, direct3d10.d3d10_shader_debug_var_info
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
req.typenames: D3D10_SHADER_DEBUG_VAR_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_VAR_INFO
 - d3d10_1shader/_D3D10_SHADER_DEBUG_VAR_INFO
 - D3D10_SHADER_DEBUG_VAR_INFO
 - d3d10_1shader/D3D10_SHADER_DEBUG_VAR_INFO
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
 - D3D10_SHADER_DEBUG_VAR_INFO
---

# D3D10_SHADER_DEBUG_VAR_INFO structure


## -description

Represents information about a shader source variable.

## -struct-fields

### -field TokenId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into token list for declaring identifier.

### -field Type

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type">D3D10_SHADER_VARIABLE_TYPE</a></b>

The variable type. <b>Type</b> is only required for arrays.

### -field Register

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Register the variable is stored in.

### -field Component

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The original variable that declared this variable.

### -field ScopeVar

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset into the scope variable array defined in <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_info">D3D10_SHADER_DEBUG_INFO</a>.

### -field ScopeVarOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

This variable's offset in its <b>ScopeVar</b>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>