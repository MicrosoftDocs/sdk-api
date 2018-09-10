---
UID: NF:d3d11shadertracing.ID3D11ShaderTrace.GetStep
title: ID3D11ShaderTrace::GetStep
author: windows-sdk-content
description: Retrieves information about the specified step in the trace.
old-location: direct3d11\id3d11shadertrace_getstep.htm
tech.root: direct3d11
ms.assetid: ECEF965F-D046-4F84-A205-F9666ECAE08C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetStep, GetStep method [Direct3D 11], GetStep method [Direct3D 11],ID3D11ShaderTrace interface, ID3D11ShaderTrace interface [Direct3D 11],GetStep method, ID3D11ShaderTrace.GetStep, ID3D11ShaderTrace::GetStep, d3d11shadertracing/ID3D11ShaderTrace::GetStep, direct3d11.id3d11shadertrace_getstep
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D11ShaderTrace.GetStep
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderTrace::GetStep


## -description


Retrieves information about the specified step in the trace.


## -parameters




### -param stepIndex [in]

The index of the step within the trace. The range of the index is [0...NumTraceSteps-1], where <b>NumTraceSteps</b> is a member of the  <a href="https://msdn.microsoft.com/en-us/library/Hh404538(v=VS.85).aspx">D3D11_TRACE_STATS</a> structure. You can retrieve information about a step in any step order.


### -param pTraceStep [out]

A pointer to a  <a href="https://msdn.microsoft.com/en-us/library/Hh404541(v=VS.85).aspx">D3D11_TRACE_STEP</a> structure. <b>GetStep</b> fills the members of this structure with information about the trace step that is specified by the <i>stepIndex</i>  parameter.


## -returns



<b>GetStep</b> returns:
        <ul>
<li><b>S_OK</b> if the method retrieves the step information.</li>
<li><b>E_FAIL</b> if a trace is not available.</li>
<li><b>E_INVALIDARG</b> if <i>stepIndex</i> is out of range or if <i>pTraceStep</i> is NULL.</li>
<li>Possibly other error codes that are described in <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.</li>
</ul>





## -remarks



This API requires the Windows Software Development Kit (SDK) for Windows 8.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh446840(v=VS.85).aspx">ID3D11ShaderTrace</a>
 

 

