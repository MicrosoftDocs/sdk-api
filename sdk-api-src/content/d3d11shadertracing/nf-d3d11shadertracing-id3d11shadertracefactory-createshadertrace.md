---
UID: NF:d3d11shadertracing.ID3D11ShaderTraceFactory.CreateShaderTrace
title: ID3D11ShaderTraceFactory::CreateShaderTrace (d3d11shadertracing.h)
description: Creates a shader-trace interface for a shader-trace information object.
helpviewer_keywords: ["CreateShaderTrace","CreateShaderTrace method [Direct3D 11]","CreateShaderTrace method [Direct3D 11]","ID3D11ShaderTraceFactory interface","ID3D11ShaderTraceFactory interface [Direct3D 11]","CreateShaderTrace method","ID3D11ShaderTraceFactory.CreateShaderTrace","ID3D11ShaderTraceFactory::CreateShaderTrace","d3d11shadertracing/ID3D11ShaderTraceFactory::CreateShaderTrace","direct3d11.id3d11shadertracefactory_createshadertrace"]
old-location: direct3d11\id3d11shadertracefactory_createshadertrace.htm
tech.root: direct3d11
ms.assetid: 8F63E8B3-0E36-49D5-AB3B-1B1C7A9B841A
ms.date: 12/05/2018
ms.keywords: CreateShaderTrace, CreateShaderTrace method [Direct3D 11], CreateShaderTrace method [Direct3D 11],ID3D11ShaderTraceFactory interface, ID3D11ShaderTraceFactory interface [Direct3D 11],CreateShaderTrace method, ID3D11ShaderTraceFactory.CreateShaderTrace, ID3D11ShaderTraceFactory::CreateShaderTrace, d3d11shadertracing/ID3D11ShaderTraceFactory::CreateShaderTrace, direct3d11.id3d11shadertracefactory_createshadertrace
req.header: d3d11shadertracing.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: D3D11SDKLayers.dll; D3D11_1SDKLayers.dll; D3D11_2SDKLayers.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ShaderTraceFactory::CreateShaderTrace
 - d3d11shadertracing/ID3D11ShaderTraceFactory::CreateShaderTrace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11SDKLayers.dll
 - D3D11_1SDKLayers.dll
 - D3D11_2SDKLayers.dll
api_name:
 - ID3D11ShaderTraceFactory.CreateShaderTrace
---

# ID3D11ShaderTraceFactory::CreateShaderTrace


## -description

Creates a shader-trace interface for a shader-trace information object.

## -parameters

### -param pShader [in]

A pointer to the interface of the shader to create the shader-trace interface for. For example, <i>pShader</i> can be an instance of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader">ID3D11VertexShader</a>, <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader">ID3D11PixelShader</a>, and so on.

### -param pTraceDesc [in]

A pointer to a  <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_shader_trace_desc">D3D11_SHADER_TRACE_DESC</a> structure that describes the shader-trace object to create. This parameter cannot be <b>NULL</b>.

### -param ppShaderTrace [out]

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/d3d11shadertracing/nn-d3d11shadertracing-id3d11shadertrace">ID3D11ShaderTrace</a> interface for the shader-trace object that <b>CreateShaderTrace</b> creates.

## -returns

<b>CreateShaderTrace</b> returns:
        <ul>
<li><b>S_OK</b> if the method created the shader-trace information object.</li>
<li><b>E_FAIL</b> if the reference device, which supports tracing, is not being used.</li>
<li><b>E_OUTOFMEMORY</b> if memory is unavailable to complete the operation.</li>
<li><b>E_INVALIDARG</b> if any parameter is NULL or invalid.</li>
<li>Possibly other error codes that are described in <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.</li>
</ul>

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/api/d3d11shadertracing/nn-d3d11shadertracing-id3d11shadertracefactory">ID3D11ShaderTraceFactory</a>