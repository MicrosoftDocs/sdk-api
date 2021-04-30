---
UID: NS:d3d11shadertracing.D3D11_TRACE_STEP
title: D3D11_TRACE_STEP (d3d11shadertracing.h)
description: Describes a trace step, which is an instruction.
helpviewer_keywords: ["D3D11_TRACE_STEP","D3D11_TRACE_STEP structure [Direct3D 11]","d3d11shadertracing/D3D11_TRACE_STEP","direct3d11.d3d11_trace_step"]
old-location: direct3d11\d3d11_trace_step.htm
tech.root: direct3d11
ms.assetid: E4C4757F-4948-41C9-97FB-446B26BE8E93
ms.date: 12/05/2018
ms.keywords: D3D11_TRACE_STEP, D3D11_TRACE_STEP structure [Direct3D 11], d3d11shadertracing/D3D11_TRACE_STEP, direct3d11.d3d11_trace_step
req.header: d3d11shadertracing.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: D3D11_TRACE_STEP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TRACE_STEP
 - d3d11shadertracing/D3D11_TRACE_STEP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11ShaderTracing.h
api_name:
 - D3D11_TRACE_STEP
---

# D3D11_TRACE_STEP structure


## -description

Describes a trace step, which is an instruction.

## -struct-fields

### -field ID

A number that identifies the instruction, as an offset into the executable instructions that are present in the shader. 

HLSL debugging information uses the same convention. Therefore, HLSL instructions are matched to a set of IDs. You can then map an ID to a disassembled string that can be displayed to the user.

### -field InstructionActive

A value that specifies whether the instruction is active. This value is TRUE if something happened; therefore, you should parse other data in this structure. Otherwise, nothing happened; for example, if an instruction is disabled due to flow control even though other pixels in the stamp execute it.

### -field NumRegistersWritten

The number of registers for the instruction that are written to. The range of registers is [0...NumRegistersWritten-1]. You can pass a register number to the <i>writtenRegisterIndex</i> parameter of  <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister">ID3D11ShaderTrace::GetWrittenRegister</a> to retrieve individual write-register information.

### -field NumRegistersRead

The number of registers for the instruction that are read from. The range of registers is [0...NumRegistersRead-1]. You can pass a register number to the <i>readRegisterIndex</i> parameter of  <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-getreadregister">ID3D11ShaderTrace::GetReadRegister</a> to retrieve individual read-register information.

### -field MiscOperations

A combination of the following values that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies the mask for the trace miscellaneous operations. These flags indicate the possible effect of a shader operation when it does not write any output registers.  For example, the "add r0, r1 ,r2" operation writes to the r0 register; therefore, you can look at the trace-written register's information to determine what the operation changed.  However, some shader instructions do not write any registers, but still effect those registers.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D11_TRACE_MISC_GS_EMIT (0x1)</td>
<td>The operation was a geometry shader data emit.</td>
</tr>
<tr>
<td>D3D11_TRACE_MISC_GS_CUT (0x2)</td>
<td>The operation was a geometry shader strip cut.</td>
</tr>
<tr>
<td>D3D11_TRACE_MISC_PS_DISCARD (0x4)</td>
<td>The operation was a pixel shader discard, which rejects the pixel.</td>
</tr>
<tr>
<td>D3D11_TRACE_MISC_GS_EMIT_STREAM (0x8)</td>
<td>Same as D3D11_TRACE_MISC_GS_EMIT, except in <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl">shader model 5</a> where you can specify a particular stream to emit to.</td>
</tr>
<tr>
<td>D3D11_TRACE_MISC_GS_CUT_STREAM (0x10)</td>
<td>Same as D3D11_TRACE_MISC_GS_CUT, except in <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl">shader model 5</a> where you can specify a particular stream to strip cut.</td>
</tr>
<tr>
<td>D3D11_TRACE_MISC_HALT (0x20)</td>
<td>The operation was a shader halt instruction, which stops shader execution. The HLSL <a href="/windows/desktop/direct3dhlsl/abort">abort</a> intrinsic function causes a halt.</td>
</tr>
<tr>
<td>D3D11_TRACE_MISC_MESSAGE (0x40)</td>
<td>The operation was a shader message output, which can be logged to the information queue. The HLSL <a href="/windows/desktop/direct3dhlsl/printf">printf</a> and <a href="/windows/desktop/direct3dhlsl/errorf">errorf</a> intrinsic functions cause messages.</td>
</tr>
</table>
 

If the <b>NumRegistersWritten</b> member is 0, examine this member although this member still might be empty (0).

### -field OpcodeType

A number that specifies the type of instruction (for example, <a href="/windows/desktop/direct3dhlsl/add---vs">add</a>, <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-mul">mul</a>, and so on). You can ignore this member if you do not know the number for the instruction type. This member offers a minor convenience at the cost of bloating the trace slightly.  You can use the <b>ID</b> member and map back to the original shader code to retrieve the full information about the instruction.

### -field CurrentGlobalCycle

The global cycle count for this step.  You can use this member to correlate parallel thread execution via multiple simultaneous traces, for example, for the compute shader.
         

<div class="alert"><b>Note</b>  Multiple threads at the same point in execution might log the same <b>CurrentGlobalCycle</b>.
         </div>
<div> </div>

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>