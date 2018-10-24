---
UID: NF:d3d11shadertracing.ID3D11ShaderTrace.ResetTrace
title: ID3D11ShaderTrace::ResetTrace
author: windows-sdk-content
description: Resets the shader-trace object.
old-location: direct3d11\id3d11shadertrace_resettrace.htm
tech.root: direct3d11
ms.assetid: 91612AEF-A83B-4B2A-960B-D7AA7F41ED41
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11ShaderTrace interface [Direct3D 11],ResetTrace method, ID3D11ShaderTrace.ResetTrace, ID3D11ShaderTrace::ResetTrace, ResetTrace, ResetTrace method [Direct3D 11], ResetTrace method [Direct3D 11],ID3D11ShaderTrace interface, d3d11shadertracing/ID3D11ShaderTrace::ResetTrace, direct3d11.id3d11shadertrace_resettrace
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
 - ID3D11ShaderTrace.ResetTrace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderTrace::ResetTrace


## -description


Resets the shader-trace object.


## -parameters






## -returns



This method has no return value.




## -remarks



After you call <b>ResetTrace</b>, the <a href="https://msdn.microsoft.com/en-us/library/Hh446840(v=VS.85).aspx">ID3D11ShaderTrace</a> object behaves as if it had just been created. Thereafter, shader invocations for the trace start from 0 again; calls to <a href="https://msdn.microsoft.com/en-us/library/Hh446865(v=VS.85).aspx">ID3D11ShaderTrace::TraceReady</a> return <b>S_FALSE</b> until the selected shader invocation number is reached, and <b>TraceReady</b> records a new trace.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh446840(v=VS.85).aspx">ID3D11ShaderTrace</a>
 

 

