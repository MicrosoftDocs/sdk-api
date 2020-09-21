---
UID: NF:d3d11shadertracing.ID3D11ShaderTrace.TraceReady
title: ID3D11ShaderTrace::TraceReady (d3d11shadertracing.h)
description: Specifies that the shader trace recorded and is ready to use.
helpviewer_keywords: ["ID3D11ShaderTrace interface [Direct3D 11]","TraceReady method","ID3D11ShaderTrace.TraceReady","ID3D11ShaderTrace::TraceReady","TraceReady","TraceReady method [Direct3D 11]","TraceReady method [Direct3D 11]","ID3D11ShaderTrace interface","d3d11shadertracing/ID3D11ShaderTrace::TraceReady","direct3d11.id3d11shadertrace_traceready"]
old-location: direct3d11\id3d11shadertrace_traceready.htm
tech.root: direct3d11
ms.assetid: BCC2BCC2-9E98-413D-B173-37664A82140B
ms.date: 12/05/2018
ms.keywords: ID3D11ShaderTrace interface [Direct3D 11],TraceReady method, ID3D11ShaderTrace.TraceReady, ID3D11ShaderTrace::TraceReady, TraceReady, TraceReady method [Direct3D 11], TraceReady method [Direct3D 11],ID3D11ShaderTrace interface, d3d11shadertracing/ID3D11ShaderTrace::TraceReady, direct3d11.id3d11shadertrace_traceready
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
 - ID3D11ShaderTrace::TraceReady
 - d3d11shadertracing/ID3D11ShaderTrace::TraceReady
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
 - ID3D11ShaderTrace.TraceReady
---

# ID3D11ShaderTrace::TraceReady


## -description

Specifies that the shader trace recorded and is ready to use.

## -parameters

### -param pTestCount [out, optional]

An optional pointer to a variable that receives the number of times that a matching invocation for the trace occurred. If not used, set to NULL.
For more information about this number, see Remarks.

## -returns

<b>TraceReady</b> returns:
        <ul>
<li><b>S_OK</b> if the trace is ready.</li>
<li><b>S_FALSE</b> if the trace is not ready.</li>
<li><b>E_OUTOFMEMORY</b> if memory ran out while the trace was in the process of recording. You can try to record the trace again by calling <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace">ID3D11ShaderTrace::ResetTrace</a> and then redrawing. If you decide not to record the trace again, release the <a href="/windows/desktop/api/d3d11shadertracing/nn-d3d11shadertracing-id3d11shadertrace">ID3D11ShaderTrace</a> interface.</li>
<li>Possibly other error codes that are described in <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.</li>
</ul>

## -remarks

If a trace is meant to record invocation 3 but only two invocations have happened so far, <b>TraceReady</b> sets the variable to which <i>pTestCount</i> points to 2.  You can use this value to understand why a trace is not ready yet. Conversely, the variable to which <i>pTestCount</i> points might be larger than the requested invocation count for a trace that is ready.  You can use this value to determine the number of invocations that ran past the required trace invocation count.  For example, you might not know the number of overdraws that occur on a pixel for a given shader in a draw call.  If you can redraw the scene identically, you can set up the traces this next time based on the value that <b>TraceReady</b> returned at <i>pTestCount</i> on the first pass.

If the shader trace recorded, you can successfully call the <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats">ID3D11ShaderTrace::GetTraceStats</a>, <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents">ID3D11ShaderTrace::GetInitialRegisterContents</a>, and  <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-getstep">ID3D11ShaderTrace::GetStep</a> methods. You can call the <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace">ID3D11ShaderTrace::ResetTrace</a> and <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-psselectstamp">ID3D11ShaderTrace::PSSelectStamp</a> methods regardless of whether the shader trace recorded.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/d3d11shadertracing/nn-d3d11shadertracing-id3d11shadertrace">ID3D11ShaderTrace</a>