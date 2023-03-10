---
UID: NS:d3d11shadertracing.D3D11_COMPUTE_SHADER_TRACE_DESC
title: D3D11_COMPUTE_SHADER_TRACE_DESC (d3d11shadertracing.h)
description: Describes an instance of a compute shader to trace.
helpviewer_keywords: ["D3D11_COMPUTE_SHADER_TRACE_DESC","D3D11_COMPUTE_SHADER_TRACE_DESC structure [Direct3D 11]","d3d11shadertracing/D3D11_COMPUTE_SHADER_TRACE_DESC","direct3d11.d3d11_compute_shader_trace_desc"]
old-location: direct3d11\d3d11_compute_shader_trace_desc.htm
tech.root: direct3d11
ms.assetid: C047CA31-22D4-4512-B90C-3C77BA6AADA9
ms.date: 12/05/2018
ms.keywords: D3D11_COMPUTE_SHADER_TRACE_DESC, D3D11_COMPUTE_SHADER_TRACE_DESC structure [Direct3D 11], d3d11shadertracing/D3D11_COMPUTE_SHADER_TRACE_DESC, direct3d11.d3d11_compute_shader_trace_desc
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
req.typenames: D3D11_COMPUTE_SHADER_TRACE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_COMPUTE_SHADER_TRACE_DESC
 - d3d11shadertracing/D3D11_COMPUTE_SHADER_TRACE_DESC
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
 - D3D11_COMPUTE_SHADER_TRACE_DESC
---

# D3D11_COMPUTE_SHADER_TRACE_DESC structure


## -description

Describes an instance of a compute shader to trace.

## -struct-fields

### -field Invocation

The invocation number of the instance of the compute shader.

### -field ThreadIDInGroup

The <a href="/windows/desktop/direct3dhlsl/sv-groupthreadid">SV_GroupThreadID</a> to trace. This value identifies indexes of individual threads within a thread group that a compute shader executes in.

### -field ThreadGroupID

The <a href="/windows/desktop/direct3dhlsl/sv-groupid">SV_GroupID</a> to trace. This value identifies indexes of a thread group that the compute shader executes in.

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>