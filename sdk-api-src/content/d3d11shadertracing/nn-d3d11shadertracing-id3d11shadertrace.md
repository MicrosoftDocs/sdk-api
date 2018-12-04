---
UID: NN:d3d11shadertracing.ID3D11ShaderTrace
title: ID3D11ShaderTrace
author: windows-sdk-content
description: An ID3D11ShaderTrace interface implements methods for obtaining traces of shader executions.
old-location: direct3d11\id3d11shadertrace.htm
tech.root: direct3d11
ms.assetid: 27FF1E53-262A-4642-A4A8-7E21163C6DF9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ID3D11ShaderTrace, ID3D11ShaderTrace interface [Direct3D 11], ID3D11ShaderTrace interface [Direct3D 11],described, d3d11shadertracing/ID3D11ShaderTrace, direct3d11.id3d11shadertrace
ms.prod: windows-hardware
ms.technology: windows-devices
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11ShaderTrace</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11ShaderTrace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/35BC4F23-64E0-4E45-A621-925A5CA20AFE">GetInitialRegisterContents</a>
</td>
<td align="left" width="63%">
Retrieves the initial contents of the specified input register.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2BDA0C25-B5D7-4A8D-A762-2C3FDF113433">GetReadRegister</a>
</td>
<td align="left" width="63%">
Retrieves information about a register that was read by a step in the trace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ECEF965F-D046-4F84-A205-F9666ECAE08C">GetStep</a>
</td>
<td align="left" width="63%">
Retrieves information about the specified step in the trace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5E61F61B-C438-4B24-8F0C-45C0583BCE08">GetTraceStats</a>
</td>
<td align="left" width="63%">
Returns statistics about the trace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/360BB797-D5A9-486A-94ED-AF1CD3A4E118">GetWrittenRegister</a>
</td>
<td align="left" width="63%">
Retrieves information about a register that was written by a step in the trace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83967A6B-E8AC-4812-8D55-62F4C065E723">PSSelectStamp</a>
</td>
<td align="left" width="63%">
Sets the specified pixel-shader stamp.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91612AEF-A83B-4B2A-960B-D7AA7F41ED41">ResetTrace</a>
</td>
<td align="left" width="63%">
Resets the shader-trace object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BCC2BCC2-9E98-413D-B173-37664A82140B">TraceReady</a>
</td>
<td align="left" width="63%">
Specifies that the shader trace recorded and is ready to use.

</td>
</tr>
</table> 


## -remarks



To retrieve an instance of <b>ID3D11ShaderTrace</b>, call the <a href="https://msdn.microsoft.com/8F63E8B3-0E36-49D5-AB3B-1B1C7A9B841A">ID3D11ShaderTraceFactory::CreateShaderTrace</a> method. To retrieve an instance of <a href="https://msdn.microsoft.com/0B90EA4B-0176-49DC-8A57-4D847552EFA3">ID3D11ShaderTraceFactory</a>, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> on a <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> that you created with <a href="d3d11_create_device_flag.htm">D3D11_CREATE_DEVICE_DEBUGGABLE</a>. Although shader tracing operates without setting <b>D3D11_CREATE_DEVICE_DEBUGGABLE</b>, we recommend that you create a shader debugging device because some devices (for example, <a href="https://msdn.microsoft.com/6daf661e-bc24-4b90-83a7-031acb57cf87">WARP</a> devices) might make behind-the-scenes shader optimizations that will lead to slightly incorrect shader traces when <b>D3D11_CREATE_DEVICE_DEBUGGABLE</b> isn't set.


All <b>ID3D11ShaderTrace</b> methods are thread safe.

All <b>ID3D11ShaderTrace</b> methods immediately force the reference device to flush rendering commands. Therefore, the most current trace status is always available on the reference device. That is, if you expect a trace to be ready after a draw operation, it will be ready.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

