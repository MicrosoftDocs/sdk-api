---
UID: NN:d3d11shadertracing.ID3D11ShaderTrace
title: ID3D11ShaderTrace
author: windows-sdk-content
description: An ID3D11ShaderTrace interface implements methods for obtaining traces of shader executions.
old-location: direct3d11\id3d11shadertrace.htm
tech.root: direct3d11
ms.assetid: 27FF1E53-262A-4642-A4A8-7E21163C6DF9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11ShaderTrace, ID3D11ShaderTrace interface [Direct3D 11], ID3D11ShaderTrace interface [Direct3D 11],described, d3d11shadertracing/ID3D11ShaderTrace, direct3d11.id3d11shadertrace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ID3D11ShaderTrace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderTrace interface


## -description


An <b>ID3D11ShaderTrace</b> interface implements methods for obtaining traces of shader executions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderTrace</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D11ShaderTrace</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11ShaderTrace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446846(v=VS.85).aspx">GetInitialRegisterContents</a>
</td>
<td align="left" width="63%">
Retrieves the initial contents of the specified input register.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446848(v=VS.85).aspx">GetReadRegister</a>
</td>
<td align="left" width="63%">
Retrieves information about a register that was read by a step in the trace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446850(v=VS.85).aspx">GetStep</a>
</td>
<td align="left" width="63%">
Retrieves information about the specified step in the trace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446853(v=VS.85).aspx">GetTraceStats</a>
</td>
<td align="left" width="63%">
Returns statistics about the trace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446856(v=VS.85).aspx">GetWrittenRegister</a>
</td>
<td align="left" width="63%">
Retrieves information about a register that was written by a step in the trace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446859(v=VS.85).aspx">PSSelectStamp</a>
</td>
<td align="left" width="63%">
Sets the specified pixel-shader stamp.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446862(v=VS.85).aspx">ResetTrace</a>
</td>
<td align="left" width="63%">
Resets the shader-trace object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446865(v=VS.85).aspx">TraceReady</a>
</td>
<td align="left" width="63%">
Specifies that the shader trace recorded and is ready to use.

</td>
</tr>
</table> 


## -remarks



To retrieve an instance of <b>ID3D11ShaderTrace</b>, call the <a href="https://msdn.microsoft.com/en-us/library/Hh446844(v=VS.85).aspx">ID3D11ShaderTraceFactory::CreateShaderTrace</a> method. To retrieve an instance of <a href="https://msdn.microsoft.com/en-us/library/Hh446842(v=VS.85).aspx">ID3D11ShaderTraceFactory</a>, call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> on a <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a> that you created with <a href="https://msdn.microsoft.com/en-us/library/Ff476107(v=VS.85).aspx">D3D11_CREATE_DEVICE_DEBUGGABLE</a>. Although shader tracing operates without setting <b>D3D11_CREATE_DEVICE_DEBUGGABLE</b>, we recommend that you create a shader debugging device because some devices (for example, <a href="https://msdn.microsoft.com/en-us/library/Ff476871(v=VS.85).aspx">WARP</a> devices) might make behind-the-scenes shader optimizations that will lead to slightly incorrect shader traces when <b>D3D11_CREATE_DEVICE_DEBUGGABLE</b> isn't set.


All <b>ID3D11ShaderTrace</b> methods are thread safe.

All <b>ID3D11ShaderTrace</b> methods immediately force the reference device to flush rendering commands. Therefore, the most current trace status is always available on the reference device. That is, if you expect a trace to be ready after a draw operation, it will be ready.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476161(v=VS.85).aspx">Shader Interfaces</a>
 

 

