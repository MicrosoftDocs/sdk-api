---
UID: NF:d3d11shadertracing.ID3D11ShaderTrace.TraceReady
title: ID3D11ShaderTrace::TraceReady
author: windows-sdk-content
description: Specifies that the shader trace recorded and is ready to use.
old-location: direct3d11\id3d11shadertrace_traceready.htm
tech.root: direct3d11
ms.assetid: BCC2BCC2-9E98-413D-B173-37664A82140B
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11ShaderTrace interface [Direct3D 11],TraceReady method, ID3D11ShaderTrace.TraceReady, ID3D11ShaderTrace::TraceReady, TraceReady, TraceReady method [Direct3D 11], TraceReady method [Direct3D 11],ID3D11ShaderTrace interface, d3d11shadertracing/ID3D11ShaderTrace::TraceReady, direct3d11.id3d11shadertrace_traceready
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
 - ID3D11ShaderTrace.TraceReady
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<li><b>E_OUTOFMEMORY</b> if memory ran out while the trace was in the process of recording. You can try to record the trace again by calling <a href="https://msdn.microsoft.com/91612AEF-A83B-4B2A-960B-D7AA7F41ED41">ID3D11ShaderTrace::ResetTrace</a> and then redrawing. If you decide not to record the trace again, release the <a href="https://msdn.microsoft.com/27FF1E53-262A-4642-A4A8-7E21163C6DF9">ID3D11ShaderTrace</a> interface.</li>
<li>Possibly other error codes that are described in <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.</li>
</ul>





## -remarks



If a trace is meant to record invocation 3 but only two invocations have happened so far, <b>TraceReady</b> sets the variable to which <i>pTestCount</i> points to 2.  You can use this value to understand why a trace is not ready yet. Conversely, the variable to which <i>pTestCount</i> points might be larger than the requested invocation count for a trace that is ready.  You can use this value to determine the number of invocations that ran past the required trace invocation count.  For example, you might not know the number of overdraws that occur on a pixel for a given shader in a draw call.  If you can redraw the scene identically, you can set up the traces this next time based on the value that <b>TraceReady</b> returned at <i>pTestCount</i> on the first pass.

If the shader trace recorded, you can successfully call the <a href="https://msdn.microsoft.com/5E61F61B-C438-4B24-8F0C-45C0583BCE08">ID3D11ShaderTrace::GetTraceStats</a>, <a href="https://msdn.microsoft.com/35BC4F23-64E0-4E45-A621-925A5CA20AFE">ID3D11ShaderTrace::GetInitialRegisterContents</a>, and  <a href="https://msdn.microsoft.com/ECEF965F-D046-4F84-A205-F9666ECAE08C">ID3D11ShaderTrace::GetStep</a> methods. You can call the <a href="https://msdn.microsoft.com/91612AEF-A83B-4B2A-960B-D7AA7F41ED41">ID3D11ShaderTrace::ResetTrace</a> and <a href="https://msdn.microsoft.com/83967A6B-E8AC-4812-8D55-62F4C065E723">ID3D11ShaderTrace::PSSelectStamp</a> methods regardless of whether the shader trace recorded.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/27FF1E53-262A-4642-A4A8-7E21163C6DF9">ID3D11ShaderTrace</a>
 

 

