---
UID: NF:d3dcompiler.D3DDisassemble
title: D3DDisassemble function (d3dcompiler.h)
description: Disassembles compiled HLSL code.
helpviewer_keywords: ["102070a9-01bc-45ad-cbcb-2ef04db4d6e7","D3DDisassemble","D3DDisassemble function [HLSL]","d3dcompiler/D3DDisassemble","direct3dhlsl.d3ddisassemble"]
old-location: direct3dhlsl\d3ddisassemble.htm
tech.root: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3ddisassemble.htm
ms.date: 12/05/2018
ms.keywords: 102070a9-01bc-45ad-cbcb-2ef04db4d6e7, D3DDisassemble, D3DDisassemble function [HLSL], d3dcompiler/D3DDisassemble, direct3dhlsl.d3ddisassemble
req.header: d3dcompiler.h
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
req.lib: D3dcompiler_47.lib
req.dll: D3dcompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DDisassemble
 - d3dcompiler/D3DDisassemble
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3dcompiler_47.dll
api_name:
 - D3DDisassemble
---

# D3DDisassemble function


## -description

Disassembles compiled HLSL code.

## -parameters

### -param pSrcData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to source data as compiled HLSL code.

### -param SrcDataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of <i>pSrcData</i>.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags affecting the behavior of <b>D3DDisassemble</b>.  <i>Flags</i> can be a combination of zero or more of the following values.
          

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td><b>D3D_DISASM_ENABLE_COLOR_CODE</b></td>
<td>Enable the output of color codes.</td>
</tr>
<tr>
<td><b>D3D_DISASM_ENABLE_DEFAULT_VALUE_PRINTS</b></td>
<td>Enable the output of default values.</td>
</tr>
<tr>
<td><b>D3D_DISASM_ENABLE_INSTRUCTION_NUMBERING</b></td>
<td>Enable instruction numbering.</td>
</tr>
<tr>
<td><b>D3D_DISASM_ENABLE_INSTRUCTION_CYCLE</b></td>
<td>No effect.</td>
</tr>
<tr>
<td><b>D3D_DISASM_DISABLE_DEBUG_INFO</b></td>
<td>Disable debug information.</td>
</tr>
<tr>
<td><b>D3D_DISASM_ENABLE_INSTRUCTION_OFFSET</b></td>
<td>Enable instruction offsets.</td>
</tr>
<tr>
<td><b>D3D_DISASM_INSTRUCTION_ONLY</b></td>
<td>Disassemble instructions only.</td>
</tr>
<tr>
<td><b> D3D_DISASM_PRINT_HEX_LITERALS</b></td>
<td>Use hex symbols in disassemblies.</td>
</tr>
</table>

### -param szComments [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The comment string at the top of the shader that identifies the shader constants and variables.

### -param ppDisassembly [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a buffer that receives the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that accesses assembly text.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>