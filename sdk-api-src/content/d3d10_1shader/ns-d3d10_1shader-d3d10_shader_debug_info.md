---
UID: NS:d3d10_1shader._D3D10_SHADER_DEBUG_INFO
title: D3D10_SHADER_DEBUG_INFO (d3d10_1shader.h)
description: Describes the format of the ID3D10Blob Interface returned by D3D10GetShaderDebugInfo.
helpviewer_keywords: ["18092958-2031-f4f8-2da4-c36244bd2989","D3D10_SHADER_DEBUG_INFO","D3D10_SHADER_DEBUG_INFO structure [Direct3D 10]","d3d10_1shader/D3D10_SHADER_DEBUG_INFO","direct3d10.d3d10_shader_debug_info"]
old-location: direct3d10\d3d10_shader_debug_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_shader_debug_info.htm
ms.date: 12/05/2018
ms.keywords: 18092958-2031-f4f8-2da4-c36244bd2989, D3D10_SHADER_DEBUG_INFO, D3D10_SHADER_DEBUG_INFO structure [Direct3D 10], d3d10_1shader/D3D10_SHADER_DEBUG_INFO, direct3d10.d3d10_shader_debug_info
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
req.typenames: D3D10_SHADER_DEBUG_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D10_SHADER_DEBUG_INFO
 - d3d10_1shader/_D3D10_SHADER_DEBUG_INFO
 - D3D10_SHADER_DEBUG_INFO
 - d3d10_1shader/D3D10_SHADER_DEBUG_INFO
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
 - D3D10_SHADER_DEBUG_INFO
---

# D3D10_SHADER_DEBUG_INFO structure


## -description

Describes the format of the <a href="/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob">ID3D10Blob Interface</a> returned by <a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getshaderdebuginfo">D3D10GetShaderDebugInfo</a>.

## -struct-fields

### -field Size

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of this structure.

### -field Creator

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to LPCSTR for compiler version.

### -field EntrypointName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to LPCSTR for Entry point name.

### -field ShaderTarget

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to LPCSTR for shader target.

### -field CompileFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags used to compile.

### -field Files

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of included files.

### -field FileInfo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to array of <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_file_info">D3D10_SHADER_DEBUG_FILE_INFO</a> structures that has <b>Files</b> elements.

### -field Instructions

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of instructions.

### -field InstructionInfo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to array of <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_inst_info">D3D10_SHADER_DEBUG_INST_INFO</a> structures that has <b>Instructions</b> elements.

### -field Variables

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of variables.

### -field VariableInfo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to array of <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_var_info">D3D10_SHADER_DEBUG_VAR_INFO</a> structures that has <b>Variables</b> elements.

### -field InputVariables

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of variables to initialize before running.

### -field InputVariableInfo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to array of <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_input_info">D3D10_SHADER_DEBUG_INPUT_INFO</a> structures that has <b>InputVariables</b> elements.

### -field Tokens

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of tokens to initialize.

### -field TokenInfo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to array of <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_token_info">D3D10_SHADER_DEBUG_TOKEN_INFO</a> structures that has <b>Tokens</b> elements.

### -field Scopes

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of scopes.

### -field ScopeInfo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to array of <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_scope_info">D3D10_SHADER_DEBUG_SCOPE_INFO</a> structures that has <b>Scopes</b> elements.

### -field ScopeVariables

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of variables declared.

### -field ScopeVariableInfo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to array of <a href="/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_scopevar_info">D3D10_SHADER_DEBUG_SCOPEVAR_INFO</a> structures that has <b>Scopes</b> elements.

### -field UintOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to the UINT datastore, all UINT offsets are from this offset.

### -field StringOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset to the string datastore, all string offsets are from this offset.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-structures">Shader Structures</a>