---
UID: NF:d3d11shadertracing.ID3D11ShaderTrace.PSSelectStamp
title: ID3D11ShaderTrace::PSSelectStamp (d3d11shadertracing.h)
description: Sets the specified pixel-shader stamp.
helpviewer_keywords: ["ID3D11ShaderTrace interface [Direct3D 11]","PSSelectStamp method","ID3D11ShaderTrace.PSSelectStamp","ID3D11ShaderTrace::PSSelectStamp","PSSelectStamp","PSSelectStamp method [Direct3D 11]","PSSelectStamp method [Direct3D 11]","ID3D11ShaderTrace interface","d3d11shadertracing/ID3D11ShaderTrace::PSSelectStamp","direct3d11.id3d11shadertrace_psselectstamp"]
old-location: direct3d11\id3d11shadertrace_psselectstamp.htm
tech.root: direct3d11
ms.assetid: 83967A6B-E8AC-4812-8D55-62F4C065E723
ms.date: 12/05/2018
ms.keywords: ID3D11ShaderTrace interface [Direct3D 11],PSSelectStamp method, ID3D11ShaderTrace.PSSelectStamp, ID3D11ShaderTrace::PSSelectStamp, PSSelectStamp, PSSelectStamp method [Direct3D 11], PSSelectStamp method [Direct3D 11],ID3D11ShaderTrace interface, d3d11shadertracing/ID3D11ShaderTrace::PSSelectStamp, direct3d11.id3d11shadertrace_psselectstamp
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
 - ID3D11ShaderTrace::PSSelectStamp
 - d3d11shadertracing/ID3D11ShaderTrace::PSSelectStamp
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
 - ID3D11ShaderTrace.PSSelectStamp
---

# ID3D11ShaderTrace::PSSelectStamp


## -description

Sets the specified pixel-shader stamp.

## -parameters

### -param stampIndex [in]

The index of the stamp to select.

## -returns

<b>PSSelectStamp</b> returns:
        <ul>
<li><b>S_OK</b> if the method set the pixel-shader stamp, and if the primitive covers the pixel and sample for the stamp.</li>
<li><b>S_FALSE</b> if the method set the pixel-shader stamp, and if the invocation for the selected stamp falls off the primitive.</li>
<li><b>E_FAIL</b> if you called the method for a vertex shader or geometry shader;   <b>PSSelectStamp</b> is meaningful only for pixel shaders.</li>
<li><b>E_INVALIDARG</b> if <i>stampIndex</i> is out of range [0..3].</li>
<li>Possibly other error codes that are described in <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.</li>
</ul>

## -remarks

After you call <b>PSSelectStamp</b> to set the pixel-shader stamp, you can call the <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents">ID3D11ShaderTrace::GetInitialRegisterContents</a>,  <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-getstep">ID3D11ShaderTrace::GetStep</a>, <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister">ID3D11ShaderTrace::GetWrittenRegister</a>, and <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-getreadregister">ID3D11ShaderTrace::GetReadRegister</a> methods to get trace data for that stamp.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/d3d11shadertracing/nn-d3d11shadertracing-id3d11shadertrace">ID3D11ShaderTrace</a>