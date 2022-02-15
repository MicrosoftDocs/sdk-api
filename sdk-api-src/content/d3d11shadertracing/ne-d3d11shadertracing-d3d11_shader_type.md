---
UID: NE:d3d11shadertracing.D3D11_SHADER_TYPE
title: D3D11_SHADER_TYPE (d3d11shadertracing.h)
description: Identifies a shader type for tracing.
helpviewer_keywords: ["D3D11_COMPUTE_SHADER","D3D11_DOMAIN_SHADER","D3D11_GEOMETRY_SHADER","D3D11_HULL_SHADER","D3D11_PIXEL_SHADER","D3D11_SHADER_TYPE","D3D11_SHADER_TYPE enumeration [Direct3D 11]","D3D11_VERTEX_SHADER","d3d11shadertracing/D3D11_COMPUTE_SHADER","d3d11shadertracing/D3D11_DOMAIN_SHADER","d3d11shadertracing/D3D11_GEOMETRY_SHADER","d3d11shadertracing/D3D11_HULL_SHADER","d3d11shadertracing/D3D11_PIXEL_SHADER","d3d11shadertracing/D3D11_SHADER_TYPE","d3d11shadertracing/D3D11_VERTEX_SHADER","direct3d11.d3d11_shader_type"]
old-location: direct3d11\d3d11_shader_type.htm
tech.root: direct3d11
ms.assetid: 4F7C8BF5-3C6E-470E-AFAA-34F4F78DAC15
ms.date: 12/05/2018
ms.keywords: D3D11_COMPUTE_SHADER, D3D11_DOMAIN_SHADER, D3D11_GEOMETRY_SHADER, D3D11_HULL_SHADER, D3D11_PIXEL_SHADER, D3D11_SHADER_TYPE, D3D11_SHADER_TYPE enumeration [Direct3D 11], D3D11_VERTEX_SHADER, d3d11shadertracing/D3D11_COMPUTE_SHADER, d3d11shadertracing/D3D11_DOMAIN_SHADER, d3d11shadertracing/D3D11_GEOMETRY_SHADER, d3d11shadertracing/D3D11_HULL_SHADER, d3d11shadertracing/D3D11_PIXEL_SHADER, d3d11shadertracing/D3D11_SHADER_TYPE, d3d11shadertracing/D3D11_VERTEX_SHADER, direct3d11.d3d11_shader_type
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
req.typenames: D3D11_SHADER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_SHADER_TYPE
 - d3d11shadertracing/D3D11_SHADER_TYPE
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
 - D3D11_SHADER_TYPE
---

# D3D11_SHADER_TYPE enumeration


## -description

Identifies a shader type for tracing.

## -enum-fields

### -field D3D11_VERTEX_SHADER:1

Identifies a vertex shader.

### -field D3D11_HULL_SHADER:2

Identifies a hull shader.

### -field D3D11_DOMAIN_SHADER:3

Identifies a domain shader.

### -field D3D11_GEOMETRY_SHADER:4

Identifies a geometry shader.

### -field D3D11_PIXEL_SHADER:5

Identifies a pixel shader.

### -field D3D11_COMPUTE_SHADER:6

Identifies a compute shader.

## -remarks

<b>D3D11_SHADER_TYPE</b> identifies the type of shader in a <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_shader_trace_desc">D3D11_SHADER_TRACE_DESC</a> structure.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-enums">Shader Enumerations</a>
