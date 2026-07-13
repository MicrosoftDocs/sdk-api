---
UID: NF:d3d11shadertracing.ID3D11ShaderTrace.ResetTrace
title: ID3D11ShaderTrace::ResetTrace (d3d11shadertracing.h)
description: Resets the shader-trace object.
helpviewer_keywords: ["ID3D11ShaderTrace interface [Direct3D 11]","ResetTrace method","ID3D11ShaderTrace.ResetTrace","ID3D11ShaderTrace::ResetTrace","ResetTrace","ResetTrace method [Direct3D 11]","ResetTrace method [Direct3D 11]","ID3D11ShaderTrace interface","d3d11shadertracing/ID3D11ShaderTrace::ResetTrace","direct3d11.id3d11shadertrace_resettrace"]
old-location: direct3d11\id3d11shadertrace_resettrace.htm
tech.root: direct3d11
ms.assetid: 91612AEF-A83B-4B2A-960B-D7AA7F41ED41
ms.date: 12/05/2018
ms.keywords: ID3D11ShaderTrace interface [Direct3D 11],ResetTrace method, ID3D11ShaderTrace.ResetTrace, ID3D11ShaderTrace::ResetTrace, ResetTrace, ResetTrace method [Direct3D 11], ResetTrace method [Direct3D 11],ID3D11ShaderTrace interface, d3d11shadertracing/ID3D11ShaderTrace::ResetTrace, direct3d11.id3d11shadertrace_resettrace
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
 - ID3D11ShaderTrace::ResetTrace
 - d3d11shadertracing/ID3D11ShaderTrace::ResetTrace
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
 - ID3D11ShaderTrace.ResetTrace
---

# ID3D11ShaderTrace::ResetTrace


## -description

Resets the shader-trace object.



## -remarks

After you call <b>ResetTrace</b>, the <a href="/windows/desktop/api/d3d11shadertracing/nn-d3d11shadertracing-id3d11shadertrace">ID3D11ShaderTrace</a> object behaves as if it had just been created. Thereafter, shader invocations for the trace start from 0 again; calls to <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-traceready">ID3D11ShaderTrace::TraceReady</a> return <b>S_FALSE</b> until the selected shader invocation number is reached, and <b>TraceReady</b> records a new trace.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/d3d11shadertracing/nn-d3d11shadertracing-id3d11shadertrace">ID3D11ShaderTrace</a>
