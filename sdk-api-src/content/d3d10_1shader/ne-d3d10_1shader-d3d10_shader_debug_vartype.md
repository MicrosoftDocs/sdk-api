---
UID: NE:d3d10_1shader._D3D10_SHADER_DEBUG_VARTYPE
title: D3D10_SHADER_DEBUG_VARTYPE (d3d10_1shader.h)
description: Distinguishes variables from functions in a scope.
helpviewer_keywords: ["D3D10_SHADER_DEBUG_VARTYPE","D3D10_SHADER_DEBUG_VARTYPE enumeration [Direct3D 10]","D3D10_SHADER_DEBUG_VAR_FORCE_DWORD","D3D10_SHADER_DEBUG_VAR_FUNCTION","D3D10_SHADER_DEBUG_VAR_VARIABLE","b5386346-ff95-5c6c-abe3-00938e5aa5ea","d3d10_1shader/D3D10_SHADER_DEBUG_VARTYPE","d3d10_1shader/D3D10_SHADER_DEBUG_VAR_FORCE_DWORD","d3d10_1shader/D3D10_SHADER_DEBUG_VAR_FUNCTION","d3d10_1shader/D3D10_SHADER_DEBUG_VAR_VARIABLE","direct3d10.d3d10_shader_debug_vartype"]
old-location: direct3d10\d3d10_shader_debug_vartype.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_vartype.htm
ms.date: 12/05/2018
ms.keywords: D3D10_SHADER_DEBUG_VARTYPE, D3D10_SHADER_DEBUG_VARTYPE enumeration [Direct3D 10], D3D10_SHADER_DEBUG_VAR_FORCE_DWORD, D3D10_SHADER_DEBUG_VAR_FUNCTION, D3D10_SHADER_DEBUG_VAR_VARIABLE, b5386346-ff95-5c6c-abe3-00938e5aa5ea, d3d10_1shader/D3D10_SHADER_DEBUG_VARTYPE, d3d10_1shader/D3D10_SHADER_DEBUG_VAR_FORCE_DWORD, d3d10_1shader/D3D10_SHADER_DEBUG_VAR_FUNCTION, d3d10_1shader/D3D10_SHADER_DEBUG_VAR_VARIABLE, direct3d10.d3d10_shader_debug_vartype
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
req.typenames: D3D10_SHADER_DEBUG_VARTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_VARTYPE
 - d3d10_1shader/_D3D10_SHADER_DEBUG_VARTYPE
 - D3D10_SHADER_DEBUG_VARTYPE
 - d3d10_1shader/D3D10_SHADER_DEBUG_VARTYPE
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
 - D3D10_SHADER_DEBUG_VARTYPE
---

# D3D10_SHADER_DEBUG_VARTYPE enumeration


## -description

Distinguishes variables from functions in a scope.

## -enum-fields

### -field D3D10_SHADER_DEBUG_VAR_VARIABLE

Element is a variable.

### -field D3D10_SHADER_DEBUG_VAR_FUNCTION

Element is a function.

### -field D3D10_SHADER_DEBUG_VAR_FORCE_DWORD:0x7fffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>
