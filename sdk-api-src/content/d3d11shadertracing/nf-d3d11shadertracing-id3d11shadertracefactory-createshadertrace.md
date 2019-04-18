---
UID: NF:d3d11shadertracing.ID3D11ShaderTraceFactory.CreateShaderTrace
title: ID3D11ShaderTraceFactory::CreateShaderTrace (d3d11shadertracing.h)
author: windows-sdk-content
description: Creates a shader-trace interface for a shader-trace information object.
old-location: direct3d11\id3d11shadertracefactory_createshadertrace.htm
tech.root: direct3d11
ms.assetid: 8F63E8B3-0E36-49D5-AB3B-1B1C7A9B841A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateShaderTrace, CreateShaderTrace method [Direct3D 11], CreateShaderTrace method [Direct3D 11],ID3D11ShaderTraceFactory interface, ID3D11ShaderTraceFactory interface [Direct3D 11],CreateShaderTrace method, ID3D11ShaderTraceFactory.CreateShaderTrace, ID3D11ShaderTraceFactory::CreateShaderTrace, d3d11shadertracing/ID3D11ShaderTraceFactory::CreateShaderTrace, direct3d11.id3d11shadertracefactory_createshadertrace
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11ShaderTraceFactory::CreateShaderTrace


## -description


Creates a shader-trace interface for a shader-trace information object.


## -parameters




### -param pShader [in]

A pointer to the interface of the shader to create the shader-trace interface for. For example, <i>pShader</i> can be an instance of <a href="https://msdn.microsoft.com/8300ec12-ecf5-49c2-9313-b542a7d971f3">ID3D11VertexShader</a>, <a href="https://msdn.microsoft.com/d16e00a9-02f9-413f-b9f7-31446fb0a692">ID3D11PixelShader</a>, and so on. 


### -param pTraceDesc [in]

A pointer to a  <a href="https://msdn.microsoft.com/0BF5D48F-EBC5-445B-B315-496C50411C72">D3D11_SHADER_TRACE_DESC</a> structure that describes the shader-trace object to create. This parameter cannot be <b>NULL</b>.


### -param ppShaderTrace [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/27FF1E53-262A-4642-A4A8-7E21163C6DF9">ID3D11ShaderTrace</a> interface for the shader-trace object that <b>CreateShaderTrace</b> creates.


## -returns



<b>CreateShaderTrace</b> returns:
        <ul>
<li><b>S_OK</b> if the method created the shader-trace information object.</li>
<li><b>E_FAIL</b> if the reference device, which supports tracing, is not being used.</li>
<li><b>E_OUTOFMEMORY</b> if memory is unavailable to complete the operation.</li>
<li><b>E_INVALIDARG</b> if any parameter is NULL or invalid.</li>
<li>Possibly other error codes that are described in <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.</li>
</ul>





## -remarks



This API requires the Windows Software Development Kit (SDK) for Windows 8.




## -see-also




<a href="https://msdn.microsoft.com/0B90EA4B-0176-49DC-8A57-4D847552EFA3">ID3D11ShaderTraceFactory</a>
 

 

