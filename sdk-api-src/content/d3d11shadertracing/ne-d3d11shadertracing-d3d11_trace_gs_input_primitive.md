---
UID: NE:d3d11shadertracing.D3D11_TRACE_GS_INPUT_PRIMITIVE
title: D3D11_TRACE_GS_INPUT_PRIMITIVE
author: windows-sdk-content
description: Identifies the type of geometry shader input primitive.
old-location: direct3d11\d3d11_trace_gs_input_primitive.htm
tech.root: direct3d11
ms.assetid: 9719D3B0-3E2E-4C0A-8CCA-4D7DA00E8FE9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_TRACE_GS_INPUT_PRIMITIVE, D3D11_TRACE_GS_INPUT_PRIMITIVE enumeration [Direct3D 11], D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE, D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE_ADJ, D3D11_TRACE_GS_INPUT_PRIMITIVE_POINT, D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE, D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE_ADJ, D3D11_TRACE_GS_INPUT_PRIMITIVE_UNDEFINED, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE_ADJ, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_POINT, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE_ADJ, d3d11shadertracing/D3D11_TRACE_GS_INPUT_PRIMITIVE_UNDEFINED, direct3d11.d3d11_trace_gs_input_primitive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11ShaderTracing.h
api_name:
 - D3D11_TRACE_GS_INPUT_PRIMITIVE
product: Windows
targetos: Windows
req.typenames: D3D11_TRACE_GS_INPUT_PRIMITIVE
req.redist: 
---

# D3D11_TRACE_GS_INPUT_PRIMITIVE enumeration


## -description


Identifies the type of geometry shader input primitive.


## -enum-fields




### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_UNDEFINED

Identifies the geometry shader input primitive as undefined.


### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_POINT

Identifies the geometry shader input primitive as a point.


### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE

Identifies the geometry shader input primitive as a line.


### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE

Identifies the geometry shader input primitive as a triangle.


### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_LINE_ADJ

Identifies the geometry shader input primitive as an adjacent line.


### -field D3D11_TRACE_GS_INPUT_PRIMITIVE_TRIANGLE_ADJ

Identifies the geometry shader input primitive as an adjacent triangle.


## -remarks



<b>D3D11_TRACE_GS_INPUT_PRIMITIVE</b> identifies the type of geometry shader input primitive in a <a href="https://msdn.microsoft.com/en-us/library/Hh404538(v=VS.85).aspx">D3D11_TRACE_STATS</a> structure.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476175(v=VS.85).aspx">Shader Enumerations</a>
 

 

