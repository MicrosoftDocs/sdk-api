---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_OUTPUTREG_INFO
title: D3D10_SHADER_DEBUG_OUTPUTREG_INFO (d3d10_1shader.h)
description: Describes a shader output register.
helpviewer_keywords: ["346fa378-bd6e-af16-a873-be0d08fda403","D3D10_SHADER_DEBUG_OUTPUTREG_INFO","D3D10_SHADER_DEBUG_OUTPUTREG_INFO structure [Direct3D 10]","d3d10_1shader/D3D10_SHADER_DEBUG_OUTPUTREG_INFO","direct3d10.d3d10_shader_debug_outputreg_info"]
old-location: direct3d10\d3d10_shader_debug_outputreg_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_outputreg_info.htm
ms.date: 12/05/2018
ms.keywords: 346fa378-bd6e-af16-a873-be0d08fda403, D3D10_SHADER_DEBUG_OUTPUTREG_INFO, D3D10_SHADER_DEBUG_OUTPUTREG_INFO structure [Direct3D 10], d3d10_1shader/D3D10_SHADER_DEBUG_OUTPUTREG_INFO, direct3d10.d3d10_shader_debug_outputreg_info
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
req.typenames: D3D10_SHADER_DEBUG_OUTPUTREG_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_OUTPUTREG_INFO
 - d3d10_1shader/_D3D10_SHADER_DEBUG_OUTPUTREG_INFO
 - D3D10_SHADER_DEBUG_OUTPUTREG_INFO
 - d3d10_1shader/D3D10_SHADER_DEBUG_OUTPUTREG_INFO
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
 - D3D10_SHADER_DEBUG_OUTPUTREG_INFO
---

# D3D10_SHADER_DEBUG_OUTPUTREG_INFO structure


## -description

Describes a shader output register.

## -struct-fields

### -field OutputRegisterSet

Type: <b><a href="/windows/win32/api/d3d10_1shader/ne-d3d10_1shader-d3d10_shader_debug_regtype">D3D10_SHADER_DEBUG_REGTYPE</a></b>

Must be D3D10_SHADER_DEBUG_REG_TEMP, D3D10_SHADER_DEBUG_REG_TEMPARRAY or D3D10_SHADER_DEBUG_REG_OUTPUT.

### -field OutputReg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value of -1 indicates no output.

### -field TempArrayReg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

If <b>OutputRegisterSet</b> is D3D10_SHADER_DEBUG_REG_TEMPARRAY this indicates which temp array.

### -field OutputComponents

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value of -1 means the component is masked out.

### -field OutputVars

Type: <b><a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_outputvar">D3D10_SHADER_DEBUG_OUTPUTVAR</a></b>

Indicates which variable the instruction is writing per-component.

### -field IndexReg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset from OutputReg of the element being written to. Used when writing to an indexable temp array or an output.

### -field IndexComp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset from OutputReg of the element being written to. Used when writing to an indexable temp array or an output.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>