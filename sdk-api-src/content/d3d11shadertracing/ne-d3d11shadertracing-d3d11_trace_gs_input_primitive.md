---
UID: NE:d3d11shadertracing.D3D11_TRACE_GS_INPUT_PRIMITIVE
title: D3D11_TRACE_GS_INPUT_PRIMITIVE (d3d11shadertracing.h)
description: Identifies the type of geometry shader input primitive.
helpviewer_keywords: ["D3D11_TRACE_GS_INPUT_PRIMITIVE","D3D11_TRACE_GS_INPUT_PRIMITIVE enumeration [Direct3D 11]","D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE","D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE_ADJ","D3D11_TRACE_GS_INPUT_PRIMITIVE_POINT","D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE","D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE_ADJ","D3D11_TRACE_GS_INPUT_PRIMITIVE_UNDEFINED","d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE","d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE","d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE_ADJ","d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_POINT","d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE","d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE_ADJ","d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_UNDEFINED","direct3d11.d3d11_trace_gs_input_primitive"]
old-location: direct3d11\d3d11_trace_gs_input_primitive.htm
tech.root: direct3d11
ms.assetid: 9719D3B0-3E2E-4C0A-8CCA-4D7DA00E8FE9
ms.date: 12/05/2018
ms.keywords: D3D11_TRACE_GS_INPUT_PRIMITIVE, D3D11_TRACE_GS_INPUT_PRIMITIVE enumeration [Direct3D 11], D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE, D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE_ADJ, D3D11_TRACE_GS_INPUT_PRIMITIVE_POINT, D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE, D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE_ADJ, D3D11_TRACE_GS_INPUT_PRIMITIVE_UNDEFINED, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE_ADJ, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_POINT, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE_ADJ, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_UNDEFINED, direct3d11.d3d11_trace_gs_input_primitive
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
req.typenames: D3D11_TRACE_GS_INPUT_PRIMITIVE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TRACE_GS_INPUT_PRIMITIVE
 - d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE
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
 - D3D11_TRACE_GS_INPUT_PRIMITIVE
---

# D3D11_TRACE_GS_INPUT_PRIMITIVE enumeration


## -description

Identifies the type of geometry shader input primitive.

## -enum-fields

### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_UNDEFINED:0

Identifies the geometry shader input primitive as undefined.

### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_POINT:1

Identifies the geometry shader input primitive as a point.

### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE:2

Identifies the geometry shader input primitive as a line.

### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE:3

Identifies the geometry shader input primitive as a triangle.

### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE_ADJ:6

Identifies the geometry shader input primitive as an adjacent line.

### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE_ADJ:7

Identifies the geometry shader input primitive as an adjacent triangle.

## -remarks

<b>D3D11_TRACE_GS_INPUT_PRIMITIVE</b> identifies the type of geometry shader input primitive in a <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_trace_stats">D3D11_TRACE_STATS</a> structure.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-enums">Shader Enumerations</a>
