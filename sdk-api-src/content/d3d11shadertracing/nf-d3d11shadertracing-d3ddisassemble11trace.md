---
UID: NF:d3d11shadertracing.D3DDisassemble11Trace
title: D3DDisassemble11Trace function (d3d11shadertracing.h)
description: Disassembles a section of compiled Microsoft High Level Shader Language (HLSL) code that is specified by shader trace steps.
helpviewer_keywords: ["D3DDisassemble11Trace","D3DDisassemble11Trace function [Direct3D 11]","d3d11shadertracing/D3DDisassemble11Trace","direct3d11.d3ddisassemble11trace"]
old-location: direct3d11\d3ddisassemble11trace.htm
tech.root: direct3d11
ms.assetid: 874A83C2-99DD-47EA-AF93-C3A47B61C4E5
ms.date: 12/05/2018
ms.keywords: D3DDisassemble11Trace, D3DDisassemble11Trace function [Direct3D 11], d3d11shadertracing/D3DDisassemble11Trace, direct3d11.d3ddisassemble11trace
req.header: d3d11shadertracing.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: D3D11SDKLayers.dll; D3D11_1SDKLayers.dll; D3D11_2SDKLayers.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DDisassemble11Trace
 - d3d11shadertracing/D3DDisassemble11Trace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D11SDKLayers.dll
 - D3D11_1SDKLayers.dll
 - D3D11_2SDKLayers.dll
api_name:
 - D3DDisassemble11Trace
---

# D3DDisassemble11Trace function


## -description

Disassembles a section of compiled Microsoft High Level Shader Language (HLSL) code that is specified by shader trace steps.

## -parameters

### -param pSrcData [in]

Type: <b>LPCVOID</b>

A pointer to compiled shader data.

### -param SrcDataSize [in]

Type: <b>SIZE_T</b>

The size, in bytes, of the block of memory that pSrcData points to.

### -param pTrace [in]

Type: <b>ID3D11ShaderTrace*</b>

A pointer to the ID3D11ShaderTrace interface for the shader trace information object.

### -param StartStep [in]

Type: <b>UINT</b>

The number of the step in the trace from which D3DDisassemble11Trace starts the disassembly.

### -param NumSteps [in]

Type: <b>UINT</b>

The number of trace steps to disassemble.

### -param Flags [in]

Type: <b>UINT</b>

A combination of zero or more of the following flags that are combined by using a bitwise OR operation. The resulting value specifies how D3DDisassemble11Trace disassembles the compiled shader data.



<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D_DISASM_ENABLE_COLOR_CODE (0x01)</td>
<td> Enable the output of color codes.</td>
</tr>
<tr>
<td>D3D_DISASM_ENABLE_DEFAULT_VALUE_PRINTS (0x02)</td>
<td> Enable the output of default values.</td>
</tr>
<tr>
<td>D3D_DISASM_ENABLE_INSTRUCTION_NUMBERING (0x04)</td>
<td> Enable instruction numbering.</td>
</tr>
<tr>
<td>D3D_DISASM_ENABLE_INSTRUCTION_CYCLE (0x08)</td>
<td> No effect.</td>
</tr>
<tr>
<td>D3D_DISASM_DISABLE_DEBUG_INFO (0x10)</td>
<td> Disable the output of debug information.</td>
</tr>
<tr>
<td>D3D_DISASM_ENABLE_INSTRUCTION_OFFSET (0x20)</td>
<td> Enable the output of instruction offsets.</td>
</tr>
<tr>
<td>D3D_DISASM_INSTRUCTION_ONLY (0x40)</td>
<td> 
Enable the output of the instruction cycle per step in D3DDisassemble11Trace. This flag is similar to the D3D_DISASM_ENABLE_INSTRUCTION_NUMBERING and D3D_DISASM_ENABLE_INSTRUCTION_OFFSET flags.

This flag has no effect in the D3DDisassembleRegion function. Cycle information comes from the trace; therefore, cycle information is available only in the trace disassembly.
 </td>
</tr>
</table>

### -param ppDisassembly [out]

Type: <b>ID3D10Blob**</b>

A pointer to a buffer that receives the ID3DBlob interface that accesses the disassembled HLSL code.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT error code.

## -remarks

D3DDisassemble11Trace walks the steps of a shader trace and outputs appropriate disassembly for each step that is based on the step's instruction index. The disassembly is annotated with register-value information from the trace. The behavior of D3DDisassemble11Trace differs from D3DDisassemble in that instead of the static disassembly of a compiled shader that D3DDisassemble performs, D3DDisassemble11Trace provides an execution trace that is based on the shader trace information.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-functions">Shader Functions</a>