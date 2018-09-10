---
UID: NN:d3d11sdklayers.ID3D11TracingDevice
title: ID3D11TracingDevice
author: windows-sdk-content
description: The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.
old-location: direct3d11\id3d11tracingdevice.htm
tech.root: direct3d11
ms.assetid: AE42E2A8-9FEE-4991-B1A0-4C6C04958DE4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11TracingDevice, ID3D11TracingDevice interface [Direct3D 11], ID3D11TracingDevice interface [Direct3D 11],described, d3d11sdklayers/ID3D11TracingDevice, direct3d11.id3d11tracingdevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11sdklayers.h
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
req.lib: D3DCompiler.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler.lib
 - D3DCompiler.dll
api_name:
 - ID3D11TracingDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11TracingDevice interface


## -description


The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11TracingDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D11TracingDevice</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11TracingDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446871(v=VS.85).aspx">SetShaderTrackingOptions</a>
</td>
<td align="left" width="63%">
Sets the reference rasterizer's race-condition tracking options for a specific shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446874(v=VS.85).aspx">SetShaderTrackingOptionsByType</a>
</td>
<td align="left" width="63%">
Sets the reference rasterizer's default race-condition tracking options for the specified resource types.

</td>
</tr>
</table> 


## -remarks



To get this interface, turn on the <a href="https://msdn.microsoft.com/en-us/library/Ff476881(v=VS.85).aspx">debug layer</a> and use <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> from the <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476158(v=VS.85).aspx">Layer Interfaces</a>
 

 

