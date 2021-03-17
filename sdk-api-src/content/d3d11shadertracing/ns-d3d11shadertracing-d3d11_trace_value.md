---
UID: NS:d3d11shadertracing.D3D11_TRACE_VALUE
title: D3D11_TRACE_VALUE (d3d11shadertracing.h)
description: Describes a trace value.
helpviewer_keywords: ["D3D11_TRACE_VALUE","D3D11_TRACE_VALUE structure [Direct3D 11]","d3d11shadertracing/D3D11_TRACE_VALUE","direct3d11.d3d11_trace_value"]
old-location: direct3d11\d3d11_trace_value.htm
tech.root: direct3d11
ms.assetid: 15AFA648-DCAC-42A1-9606-6E292E92C217
ms.date: 12/05/2018
ms.keywords: D3D11_TRACE_VALUE, D3D11_TRACE_VALUE structure [Direct3D 11], d3d11shadertracing/D3D11_TRACE_VALUE, direct3d11.d3d11_trace_value
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
req.typenames: D3D11_TRACE_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TRACE_VALUE
 - d3d11shadertracing/D3D11_TRACE_VALUE
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
 - D3D11_TRACE_VALUE
---

# D3D11_TRACE_VALUE structure


## -description

Describes a trace value.

## -struct-fields

### -field Bits

An array of bits that make up the trace value. The [0] element is X.
            

<div class="alert"><b>Note</b>  This member can hold <b>float</b>, <b>UINT</b>, or <b>INT</b> data.
              The elements are specified as <b>UINT</b> rather than using a union to minimize the risk of x86 SNaN-&gt;QNaN quashing during float assignment.
              If the bits are displayed, they can be interpreted as <b>float</b> at the last moment.
            </div>
<div> </div>

### -field ValidMask

A combination of the following component values that are combined by using a bitwise <b>OR</b> operation.
            The resulting value specifies the component trace mask.
            

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D11_TRACE_COMPONENT_X (0x1)</td>
<td>The x component of the trace mask.</td>
</tr>
<tr>
<td>D3D11_TRACE_COMPONENT_Y (0x2)</td>
<td>The y component of the trace mask.</td>
</tr>
<tr>
<td>D3D11_TRACE_COMPONENT_Z (0x4)</td>
<td>The depth z component of the trace mask.</td>
</tr>
<tr>
<td>D3D11_TRACE_COMPONENT_W (0x8)</td>
<td>The depth w component of the trace mask.</td>
</tr>
</table>
 

Ignore unmasked values, particularly if deltas are accumulated.

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>