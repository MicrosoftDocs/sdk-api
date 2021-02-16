---
UID: NF:d3d11shadertracing.ID3D11ShaderTrace.GetReadRegister
title: ID3D11ShaderTrace::GetReadRegister (d3d11shadertracing.h)
description: Retrieves information about a register that was read by a step in the trace.
helpviewer_keywords: ["GetReadRegister","GetReadRegister method [Direct3D 11]","GetReadRegister method [Direct3D 11]","ID3D11ShaderTrace interface","ID3D11ShaderTrace interface [Direct3D 11]","GetReadRegister method","ID3D11ShaderTrace.GetReadRegister","ID3D11ShaderTrace::GetReadRegister","d3d11shadertracing/ID3D11ShaderTrace::GetReadRegister","direct3d11.id3d11shadertrace_getreadregister"]
old-location: direct3d11\id3d11shadertrace_getreadregister.htm
tech.root: direct3d11
ms.assetid: 2BDA0C25-B5D7-4A8D-A762-2C3FDF113433
ms.date: 12/05/2018
ms.keywords: GetReadRegister, GetReadRegister method [Direct3D 11], GetReadRegister method [Direct3D 11],ID3D11ShaderTrace interface, ID3D11ShaderTrace interface [Direct3D 11],GetReadRegister method, ID3D11ShaderTrace.GetReadRegister, ID3D11ShaderTrace::GetReadRegister, d3d11shadertracing/ID3D11ShaderTrace::GetReadRegister, direct3d11.id3d11shadertrace_getreadregister
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
 - ID3D11ShaderTrace::GetReadRegister
 - d3d11shadertracing/ID3D11ShaderTrace::GetReadRegister
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
 - ID3D11ShaderTrace.GetReadRegister
---

# ID3D11ShaderTrace::GetReadRegister


## -description

Retrieves information about a register that was read by a step in the trace.

## -parameters

### -param stepIndex [in]

The index of the step within the trace. The range of the index is [0...NumTraceSteps-1], where <b>NumTraceSteps</b> is a member of the  <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_trace_stats">D3D11_TRACE_STATS</a> structure. You can retrieve information in any step order.

### -param readRegisterIndex [in]

The index of the register within  the trace step. The range of the index is [0...NumRegistersRead-1], where <b>NumRegistersRead</b> is a member of the  <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_trace_step">D3D11_TRACE_STEP</a> structure.

### -param pRegister [out]

A pointer to a <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_trace_register">D3D11_TRACE_REGISTER</a> structure. <b>GetReadRegister</b> fills the members of this structure with information about the register that was read by the step in the trace.

### -param pValue [out]

A pointer to a  <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_trace_value">D3D11_TRACE_VALUE</a> structure. <b>GetReadRegister</b> fills the members of this structure with information about the value that was read from the register.

## -returns

<b>GetReadRegister</b> returns:
        <ul>
<li><b>S_OK</b> if the method retrieves the register information.</li>
<li><b>E_FAIL</b> if a trace is not available or if the trace was not created with the D3D11_SHADER_TRACE_FLAG_RECORD_REGISTER_READS flag.</li>
<li><b>E_INVALIDARG</b> if <i>stepIndex</i> or <i>readRegisterIndex</i> is out of range or if <i>pRegister</i> or <i>pValue</i> is NULL.</li>
<li>Possibly other error codes that are described in <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.</li>
</ul>

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/api/d3d11shadertracing/nn-d3d11shadertracing-id3d11shadertrace">ID3D11ShaderTrace</a>