---
UID: NN:d3d11sdklayers.ID3D11TracingDevice
title: ID3D11TracingDevice
author: windows-sdk-content
description: The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.
old-location: direct3d11\id3d11tracingdevice.htm
tech.root: direct3d11
ms.assetid: AE42E2A8-9FEE-4991-B1A0-4C6C04958DE4
ms.author: windowssdkdev
ms.date: 08/30/2018
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11TracingDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11TracingDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/F62FCA38-AE44-427B-95B4-252AE800845C">SetShaderTrackingOptions</a>
</td>
<td align="left" width="63%">
Sets the reference rasterizer's race-condition tracking options for a specific shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ABB83CE4-D612-4797-A9AD-F3C2954E669D">SetShaderTrackingOptionsByType</a>
</td>
<td align="left" width="63%">
Sets the reference rasterizer's default race-condition tracking options for the specified resource types.

</td>
</tr>
</table> 


## -remarks



To get this interface, turn on the <a href="overviews_direct3d_11_devices_layers.htm">debug layer</a> and use <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> from the <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d">Layer Interfaces</a>
 

 

