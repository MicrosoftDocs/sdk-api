---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_OUTPUTVAR
title: D3D10_SHADER_DEBUG_OUTPUTVAR (d3d10_1shader.h)
description: Describes a shader output variable.
helpviewer_keywords: ["D3D10_SHADER_DEBUG_OUTPUTVAR","D3D10_SHADER_DEBUG_OUTPUTVAR structure [Direct3D 10]","a188f87a-61c2-dda1-1e50-d2cbcbeb680f","d3d10_1shader/D3D10_SHADER_DEBUG_OUTPUTVAR","direct3d10.d3d10_shader_debug_outputvar"]
old-location: direct3d10\d3d10_shader_debug_outputvar.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_outputvar.htm
ms.date: 12/05/2018
ms.keywords: D3D10_SHADER_DEBUG_OUTPUTVAR, D3D10_SHADER_DEBUG_OUTPUTVAR structure [Direct3D 10], a188f87a-61c2-dda1-1e50-d2cbcbeb680f, d3d10_1shader/D3D10_SHADER_DEBUG_OUTPUTVAR, direct3d10.d3d10_shader_debug_outputvar
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
req.typenames: D3D10_SHADER_DEBUG_OUTPUTVAR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_OUTPUTVAR
 - d3d10_1shader/_D3D10_SHADER_DEBUG_OUTPUTVAR
 - D3D10_SHADER_DEBUG_OUTPUTVAR
 - d3d10_1shader/D3D10_SHADER_DEBUG_OUTPUTVAR
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
 - D3D10_SHADER_DEBUG_OUTPUTVAR
---

# D3D10_SHADER_DEBUG_OUTPUTVAR structure


## -description

Describes a shader output variable.

## -struct-fields

### -field Var

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index variable being written to or if -1 it's not going to a variable.

### -field uValueMin

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Minimum UINT value.

### -field uValueMax

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Maximum UINT value.

### -field iValueMin

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Minimum INT value.

### -field iValueMax

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Maximum UINT value.

### -field fValueMin

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Minimum FLOAT value.

### -field fValueMax

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Maximum FLOAT value.

### -field bNaNPossible

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Indicates whether the output variable can evaluate to not a number.

### -field bInfPossible

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Indicates whether the output variable can evaluate to infinity.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>