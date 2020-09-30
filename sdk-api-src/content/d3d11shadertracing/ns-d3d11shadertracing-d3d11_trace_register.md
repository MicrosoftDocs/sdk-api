---
UID: NS:d3d11shadertracing.D3D11_TRACE_REGISTER
title: D3D11_TRACE_REGISTER (d3d11shadertracing.h)
description: Describes a trace register.
helpviewer_keywords: ["D3D11_TRACE_REGISTER","D3D11_TRACE_REGISTER structure [Direct3D 11]","d3d11shadertracing/D3D11_TRACE_REGISTER","direct3d11.d3d11_trace_register"]
old-location: direct3d11\d3d11_trace_register.htm
tech.root: direct3d11
ms.assetid: 32A51FC7-375D-40BE-95F2-65C5057F002C
ms.date: 12/05/2018
ms.keywords: D3D11_TRACE_REGISTER, D3D11_TRACE_REGISTER structure [Direct3D 11], d3d11shadertracing/D3D11_TRACE_REGISTER, direct3d11.d3d11_trace_register
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
req.typenames: D3D11_TRACE_REGISTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TRACE_REGISTER
 - d3d11shadertracing/D3D11_TRACE_REGISTER
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
 - D3D11_TRACE_REGISTER
---

# D3D11_TRACE_REGISTER structure


## -description

Describes a trace register.

## -struct-fields

### -field RegType

A <a href="/windows/desktop/api/d3d11shadertracing/ne-d3d11shadertracing-d3d11_trace_register_type">D3D11_TRACE_REGISTER_TYPE</a>-typed value that identifies the type of register that the shader-trace object uses.

### -field Index1D

An index for one-dimensional arrays. This index is used by the following register types: 

<ul>
<li>vertex shader or pixel shader input: v[Index1D]</li>
<li>temp: r[Index1D]</li>
<li>output: o[Index1D]</li>
<li>immediate constant buffer: icb[Index1D]</li>
<li>sampler s[Index1D]</li>
<li>resource r[Index1D]</li>
<li>input patch constant register: vpc[Index1D] </li>
<li>unordered access view: u[Index1D]</li>
<li>thread group shared memory: g[Index1D]</li>
</ul>

### -field Index2D

An array of indexes for two-dimensional arrays. These indexes are used by the following register types:

<ul>
<li>GS input: v[Index2D[0]][Index2D[1]]</li>
<li>indexable temp: x[Index2D[0]][Index2D[1]]</li>
<li>constant buffer: cb#[#]</li>
<li>input control point register: vcp[Index2D[0]][Index2D[1]]</li>
<li>output control point register: vocp[Index2D[0]][Index2D[1]]</li>
</ul>

### -field OperandIndex

The index of the operand, which starts from 0.

### -field Flags

A combination of the following flags that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies more about the trace register.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D11_TRACE_REGISTER_FLAGS_RELATIVE_INDEXING (0x1)</td>
<td>Access to the register is part of the relative indexing of a register.</td>
</tr>
</table>

## -remarks

The following register types do not require an index:

<ul>
<li>input PrimitiveID</li>
<li>output oDepth</li>
<li>immediate32</li>
<li>NULL register</li>
<li>output control point ID (this is actually an input; it defines the output that the thread controls)</li>
<li>input fork instance ID</li>
<li>input join instance ID</li>
<li>input domain point register</li>
<li>cycle counter</li>
</ul>
<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>