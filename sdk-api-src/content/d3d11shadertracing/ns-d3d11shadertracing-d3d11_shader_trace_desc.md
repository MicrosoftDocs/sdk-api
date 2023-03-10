---
UID: NS:d3d11shadertracing.D3D11_SHADER_TRACE_DESC
title: D3D11_SHADER_TRACE_DESC (d3d11shadertracing.h)
description: Describes a shader-trace object.
helpviewer_keywords: ["D3D11_SHADER_TRACE_DESC","D3D11_SHADER_TRACE_DESC structure [Direct3D 11]","d3d11shadertracing/D3D11_SHADER_TRACE_DESC","direct3d11.d3d11_shader_trace_desc"]
old-location: direct3d11\d3d11_shader_trace_desc.htm
tech.root: direct3d11
ms.assetid: 0BF5D48F-EBC5-445B-B315-496C50411C72
ms.date: 12/05/2018
ms.keywords: D3D11_SHADER_TRACE_DESC, D3D11_SHADER_TRACE_DESC structure [Direct3D 11], d3d11shadertracing/D3D11_SHADER_TRACE_DESC, direct3d11.d3d11_shader_trace_desc
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
req.typenames: D3D11_SHADER_TRACE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_SHADER_TRACE_DESC
 - d3d11shadertracing/D3D11_SHADER_TRACE_DESC
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
 - D3D11_SHADER_TRACE_DESC
---

# D3D11_SHADER_TRACE_DESC structure


## -description

Describes a shader-trace object.

## -struct-fields

### -field Type

A <a href="/windows/desktop/api/d3d11shadertracing/ne-d3d11shadertracing-d3d11_shader_type">D3D11_SHADER_TYPE</a>-typed value that identifies the type of shader that the shader-trace object describes. This member also determines which shader-trace type to use in the following union.

### -field Flags

A combination of the following flags that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace">ID3D11ShaderTraceFactory::CreateShaderTrace</a> creates the shader-trace object.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D11_SHADER_TRACE_FLAG_RECORD_REGISTER_WRITES (0x1)</td>
<td>The shader trace object records register-writes.</td>
</tr>
<tr>
<td>D3D11_SHADER_TRACE_FLAG_RECORD_REGISTER_READS (0x2)</td>
<td>The shader trace object records register-reads.</td>
</tr>
</table>

### -field VertexShaderTraceDesc

A <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc">D3D11_VERTEX_SHADER_TRACE_DESC</a> structure that describes an instance of a vertex shader to trace.

### -field HullShaderTraceDesc

A <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc">D3D11_HULL_SHADER_TRACE_DESC</a> structure that describes an instance of a hull shader to trace.

### -field DomainShaderTraceDesc

A <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc">D3D11_DOMAIN_SHADER_TRACE_DESC</a> structure that describes an instance of a domain shader to trace.

### -field GeometryShaderTraceDesc

A <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc">D3D11_GEOMETRY_SHADER_TRACE_DESC</a> structure that describes an instance of a geometry shader to trace.

### -field PixelShaderTraceDesc

A <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc">D3D11_PIXEL_SHADER_TRACE_DESC</a> structure that describes an instance of a pixel shader to trace.

### -field ComputeShaderTraceDesc

A <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc">D3D11_COMPUTE_SHADER_TRACE_DESC</a> structure that describes an instance of a compute shader to trace.

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace">ID3D11ShaderTraceFactory::CreateShaderTrace</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>