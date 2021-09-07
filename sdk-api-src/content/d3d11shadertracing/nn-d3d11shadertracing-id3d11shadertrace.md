---
UID: NN:d3d11shadertracing.ID3D11ShaderTrace
title: ID3D11ShaderTrace (d3d11shadertracing.h)
description: An ID3D11ShaderTrace interface implements methods for obtaining traces of shader executions.
helpviewer_keywords: ["ID3D11ShaderTrace","ID3D11ShaderTrace interface [Direct3D 11]","ID3D11ShaderTrace interface [Direct3D 11]","described","d3d11shadertracing/ID3D11ShaderTrace","direct3d11.id3d11shadertrace"]
old-location: direct3d11\id3d11shadertrace.htm
tech.root: direct3d11
ms.assetid: 27FF1E53-262A-4642-A4A8-7E21163C6DF9
ms.date: 12/05/2018
ms.keywords: ID3D11ShaderTrace, ID3D11ShaderTrace interface [Direct3D 11], ID3D11ShaderTrace interface [Direct3D 11],described, d3d11shadertracing/ID3D11ShaderTrace, direct3d11.id3d11shadertrace
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
 - ID3D11ShaderTrace
 - d3d11shadertracing/ID3D11ShaderTrace
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
 - ID3D11ShaderTrace
---

# ID3D11ShaderTrace interface


## -description

An <b>ID3D11ShaderTrace</b> interface implements methods for obtaining traces of shader executions.

## -inheritance

The <b>ID3D11ShaderTrace</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ShaderTrace</b> also has these types of members:

## -remarks

To retrieve an instance of <b>ID3D11ShaderTrace</b>, call the <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace">ID3D11ShaderTraceFactory::CreateShaderTrace</a> method. To retrieve an instance of <a href="/windows/desktop/api/d3d11shadertracing/nn-d3d11shadertracing-id3d11shadertracefactory">ID3D11ShaderTraceFactory</a>, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> on a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> that you created with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_DEBUGGABLE</a>. Although shader tracing operates without setting <b>D3D11_CREATE_DEVICE_DEBUGGABLE</b>, we recommend that you create a shader debugging device because some devices (for example, <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp">WARP</a> devices) might make behind-the-scenes shader optimizations that will lead to slightly incorrect shader traces when <b>D3D11_CREATE_DEVICE_DEBUGGABLE</b> isn't set.


All <b>ID3D11ShaderTrace</b> methods are thread safe.

All <b>ID3D11ShaderTrace</b> methods immediately force the reference device to flush rendering commands. Therefore, the most current trace status is always available on the reference device. That is, if you expect a trace to be ready after a draw operation, it will be ready.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
