---
UID: NF:d3dcompiler.D3DGetTraceInstructionOffsets
title: D3DGetTraceInstructionOffsets function (d3dcompiler.h)
description: Retrieves the byte offsets for instructions within a section of shader code.
helpviewer_keywords: ["D3DGetTraceInstructionOffsets","D3DGetTraceInstructionOffsets function [HLSL]","d3dcompiler/D3DGetTraceInstructionOffsets","direct3dhlsl.d3dgettraceinstructionoffsets"]
old-location: direct3dhlsl\d3dgettraceinstructionoffsets.htm
tech.root: direct3dhlsl
ms.assetid: 9E27C70C-C266-48A6-81C7-E9A5E430B48B
ms.date: 12/05/2018
ms.keywords: D3DGetTraceInstructionOffsets, D3DGetTraceInstructionOffsets function [HLSL], d3dcompiler/D3DGetTraceInstructionOffsets, direct3dhlsl.d3dgettraceinstructionoffsets
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DGetTraceInstructionOffsets
 - d3dcompiler/D3DGetTraceInstructionOffsets
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DGetTraceInstructionOffsets
---

# D3DGetTraceInstructionOffsets function


## -description

Retrieves the byte offsets for instructions within a section of shader code.

## -parameters

### -param pSrcData [in]

A pointer to the compiled shader data.

### -param SrcDataSize [in]

The size, in bytes, of the block of memory that <i>pSrcData</i> points to.

### -param Flags [in]

A combination of the following flags that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how <b>D3DGetTraceInstructionOffsets</b> retrieves the instruction offsets.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D_GET_INST_OFFSETS_INCLUDE_NON_EXECUTABLE (0x01)</td>
<td>Include non-executable code in the retrieved information.</td>
</tr>
</table>

### -param StartInstIndex [in]

The index of the instruction in the compiled shader data for which <b>D3DGetTraceInstructionOffsets</b> starts to retrieve the byte offsets.

### -param NumInsts [in]

The number of instructions for which <b>D3DGetTraceInstructionOffsets</b> retrieves the byte offsets.

### -param pOffsets [out, optional]

A pointer to a variable that receives the actual number of offsets.

### -param pTotalInsts [out, optional]

A pointer to a variable that receives the total number of instructions in the section of shader code.

## -returns

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

A new kind of Microsoft High Level Shader Language (HLSL) debugging information from a program database (PDB) file uses instruction-byte offsets within a shader blob (arbitrary-length data buffer). You use <b>D3DGetTraceInstructionOffsets</b> to translate to and from instruction indexes.

<div class="alert"><b>Note</b>  The D3dcompiler_44.dll or later version of the file contains the <b>D3DGetTraceInstructionOffsets</b> compiler function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>