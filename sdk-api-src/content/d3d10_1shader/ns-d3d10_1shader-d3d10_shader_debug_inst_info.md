---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_INST_INFO
title: D3D10_SHADER_DEBUG_INST_INFO (d3d10_1shader.h)
description: Contains instruction data.
helpviewer_keywords: ["D3D10_SHADER_DEBUG_INST_INFO","D3D10_SHADER_DEBUG_INST_INFO structure [Direct3D 10]","be8000a0-f3a0-c087-b23f-aeedd69d29d6","d3d10_1shader/D3D10_SHADER_DEBUG_INST_INFO","direct3d10.d3d10_shader_debug_inst_info"]
old-location: direct3d10\d3d10_shader_debug_inst_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_inst_info.htm
ms.date: 12/05/2018
ms.keywords: D3D10_SHADER_DEBUG_INST_INFO, D3D10_SHADER_DEBUG_INST_INFO structure [Direct3D 10], be8000a0-f3a0-c087-b23f-aeedd69d29d6, d3d10_1shader/D3D10_SHADER_DEBUG_INST_INFO, direct3d10.d3d10_shader_debug_inst_info
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
req.typenames: D3D10_SHADER_DEBUG_INST_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_INST_INFO
 - d3d10_1shader/_D3D10_SHADER_DEBUG_INST_INFO
 - D3D10_SHADER_DEBUG_INST_INFO
 - d3d10_1shader/D3D10_SHADER_DEBUG_INST_INFO
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
 - D3D10_SHADER_DEBUG_INST_INFO
---

# D3D10_SHADER_DEBUG_INST_INFO structure


## -description

Contains instruction data.

## -struct-fields

### -field Id

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Id of the instruction.

### -field Opcode

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Type of instruction.

### -field uOutputs

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Must be 0, 1 or 2.

### -field pOutputs

Type: <b><a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_outputreg_info">D3D10_SHADER_DEBUG_OUTPUTREG_INFO</a></b>

Array containing the outputs of the instruction.

### -field TokenId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the list of tokens for this instruction's token.

### -field NestingLevel

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of function calls deep this instruction is.

### -field Scopes

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of scopes.

### -field ScopeInfo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to an array of UINT values with <b>Scopes</b> elements.

### -field AccessedVars

### -field AccessedVarsInfo

## -remarks

The <b>D3D10_SHADER_DEBUG_INST_INFO</b> structure is used with the <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_info">D3D10_SHADER_DEBUG_INFO</a> structure.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>