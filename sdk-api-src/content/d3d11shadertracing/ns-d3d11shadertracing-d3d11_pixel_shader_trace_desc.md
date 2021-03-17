---
UID: NS:d3d11shadertracing.D3D11_PIXEL_SHADER_TRACE_DESC
title: D3D11_PIXEL_SHADER_TRACE_DESC (d3d11shadertracing.h)
description: Describes an instance of a pixel shader to trace.
helpviewer_keywords: ["D3D11_PIXEL_SHADER_TRACE_DESC","D3D11_PIXEL_SHADER_TRACE_DESC structure [Direct3D 11]","d3d11shadertracing/D3D11_PIXEL_SHADER_TRACE_DESC","direct3d11.d3d11_pixel_shader_trace_desc"]
old-location: direct3d11\d3d11_pixel_shader_trace_desc.htm
tech.root: direct3d11
ms.assetid: 4A44DA4F-81FC-47BE-90CA-06355C363795
ms.date: 12/05/2018
ms.keywords: D3D11_PIXEL_SHADER_TRACE_DESC, D3D11_PIXEL_SHADER_TRACE_DESC structure [Direct3D 11], d3d11shadertracing/D3D11_PIXEL_SHADER_TRACE_DESC, direct3d11.d3d11_pixel_shader_trace_desc
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
req.typenames: D3D11_PIXEL_SHADER_TRACE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_PIXEL_SHADER_TRACE_DESC
 - d3d11shadertracing/D3D11_PIXEL_SHADER_TRACE_DESC
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
 - D3D11_PIXEL_SHADER_TRACE_DESC
---

# D3D11_PIXEL_SHADER_TRACE_DESC structure


## -description

Describes an instance of a pixel shader to trace.

## -struct-fields

### -field Invocation

The invocation number of the instance of the pixel shader.

### -field X

The x-coordinate of the pixel.

### -field Y

The y-coordinate of the pixel.

### -field SampleMask

A value that describes a mask of pixel samples to trace. If this value specifies any of the masked samples, the trace is activated.  The least significant bit (LSB) is sample 0.  The non-multisample antialiasing (MSAA) counts as a sample count of 1; therefore, the LSB of <b>SampleMask</b> should be set. If set to zero, the pixel is not traced. However, pixel traces can still be enabled on an invocation basis.

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>