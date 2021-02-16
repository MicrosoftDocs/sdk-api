---
UID: NF:d3d11shadertracing.ID3D11ShaderTrace.GetTraceStats
title: ID3D11ShaderTrace::GetTraceStats (d3d11shadertracing.h)
description: Returns statistics about the trace.
helpviewer_keywords: ["GetTraceStats","GetTraceStats method [Direct3D 11]","GetTraceStats method [Direct3D 11]","ID3D11ShaderTrace interface","ID3D11ShaderTrace interface [Direct3D 11]","GetTraceStats method","ID3D11ShaderTrace.GetTraceStats","ID3D11ShaderTrace::GetTraceStats","d3d11shadertracing/ID3D11ShaderTrace::GetTraceStats","direct3d11.id3d11shadertrace_gettracestats"]
old-location: direct3d11\id3d11shadertrace_gettracestats.htm
tech.root: direct3d11
ms.assetid: 5E61F61B-C438-4B24-8F0C-45C0583BCE08
ms.date: 12/05/2018
ms.keywords: GetTraceStats, GetTraceStats method [Direct3D 11], GetTraceStats method [Direct3D 11],ID3D11ShaderTrace interface, ID3D11ShaderTrace interface [Direct3D 11],GetTraceStats method, ID3D11ShaderTrace.GetTraceStats, ID3D11ShaderTrace::GetTraceStats, d3d11shadertracing/ID3D11ShaderTrace::GetTraceStats, direct3d11.id3d11shadertrace_gettracestats
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
 - ID3D11ShaderTrace::GetTraceStats
 - d3d11shadertracing/ID3D11ShaderTrace::GetTraceStats
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
 - ID3D11ShaderTrace.GetTraceStats
---

# ID3D11ShaderTrace::GetTraceStats


## -description

Returns statistics about the trace.

## -parameters

### -param pTraceStats [out]

A pointer to a <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_trace_stats">D3D11_TRACE_STATS</a> structure. <b>GetTraceStats</b> fills the members of this structure with statistics about the trace.

## -returns

<b>GetTraceStats</b> returns:
        <ul>
<li>S_OK if statistics about the trace are successfully obtained.</li>
<li>E_FAIL if no trace statistics are available yet; <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-traceready">ID3D11ShaderTrace::TraceReady</a> must return S_OK before <b>GetTraceStats</b> can succeed.</li>
<li>E_INVALIDARG if <i>pTraceStats</i> is NULL.</li>
<li>Possibly other error codes that are described in <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.</li>
</ul>

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/api/d3d11shadertracing/nn-d3d11shadertracing-id3d11shadertrace">ID3D11ShaderTrace</a>