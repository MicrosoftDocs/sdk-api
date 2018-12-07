---
UID: NF:d3dcompiler.D3DDisassembleRegion
title: D3DDisassembleRegion function
author: windows-sdk-content
description: Disassembles a specific region of compiled Microsoft High Level Shader Language (HLSL) code.
old-location: direct3dhlsl\d3ddisassembleregion.htm
tech.root: direct3dhlsl
ms.assetid: 4813FF62-42FA-425D-9C24-9E472F04E35B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3DDisassembleRegion, D3DDisassembleRegion function [HLSL], d3dcompiler/D3DDisassembleRegion, direct3dhlsl.d3ddisassembleregion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DDisassembleRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3DDisassembleRegion function


## -description


Disassembles a specific region of compiled Microsoft High Level Shader Language (HLSL) code.


## -parameters




### -param pSrcData [in]

A pointer to compiled shader data.


### -param SrcDataSize [in]

The size, in bytes, of the block of memory that <i>pSrcData</i> points to.


### -param Flags [in]

A combination of zero or more of the following flags that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how <b>D3DDisassembleRegion</b> disassembles the compiled shader data.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D_DISASM_ENABLE_COLOR_CODE (0x01)</td>
<td>Enable the output of color codes.</td>
</tr>
<tr>
<td>D3D_DISASM_ENABLE_DEFAULT_VALUE_PRINTS (0x02)</td>
<td>Enable the output of default values.</td>
</tr>
<tr>
<td>D3D_DISASM_ENABLE_INSTRUCTION_NUMBERING (0x04)</td>
<td>Enable instruction numbering.</td>
</tr>
<tr>
<td>D3D_DISASM_ENABLE_INSTRUCTION_CYCLE (0x08)</td>
<td>No effect.</td>
</tr>
<tr>
<td>D3D_DISASM_DISABLE_DEBUG_INFO (0x10)</td>
<td>Disable the output of debug information.</td>
</tr>
<tr>
<td>D3D_DISASM_ENABLE_INSTRUCTION_OFFSET (0x20)</td>
<td>Enable the output of instruction offsets.</td>
</tr>
<tr>
<td>D3D_DISASM_INSTRUCTION_ONLY (0x40)</td>
<td>This flag has no effect in <b>D3DDisassembleRegion</b>. Cycle information comes from the trace; therefore, cycle information is available only in <a href="https://msdn.microsoft.com/983D5530-E220-42BE-9210-16E5A789CEE1">D3DDisassemble11Trace</a>'s trace disassembly.</td>
</tr>
</table>
 


### -param szComments [in, optional]

A pointer to a constant null-terminated string at the top of the shader that identifies the shader constants and variables.


### -param StartByteOffset [in]

The number of bytes offset into the compiled shader data where <b>D3DDisassembleRegion</b> starts the disassembly.


### -param NumInsts [in]

The number of instructions to disassemble.


### -param pFinishByteOffset [out, optional]

A pointer to a variable that receives the number of bytes offset into the compiled shader data where <b>D3DDisassembleRegion</b> finishes the disassembly.


### -param ppDisassembly [out]

A pointer to a buffer that receives the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that accesses the disassembled HLSL code.


## -returns



Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



<div class="alert"><b>Note</b>  The D3dcompiler_44.dll or later version of the file contains the <b>D3DDisassembleRegion</b> compiler function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd607342(v=VS.85).aspx">Functions</a>
 

 

