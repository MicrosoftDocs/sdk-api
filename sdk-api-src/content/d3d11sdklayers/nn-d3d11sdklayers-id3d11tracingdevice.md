---
UID: NN:d3d11sdklayers.ID3D11TracingDevice
title: ID3D11TracingDevice (d3d11sdklayers.h)
author: windows-sdk-content
description: The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.
old-location: direct3d11\id3d11tracingdevice.htm
tech.root: direct3d11
ms.assetid: AE42E2A8-9FEE-4991-B1A0-4C6C04958DE4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11TracingDevice, ID3D11TracingDevice interface [Direct3D 11], ID3D11TracingDevice interface [Direct3D 11],described, d3d11sdklayers/ID3D11TracingDevice, direct3d11.id3d11tracingdevice
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
ms.custom: 19H1
---

# ID3D11TracingDevice interface


## -description


The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11TracingDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11TracingDevice</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptions">SetShaderTrackingOptions</a>
</td>
<td align="left" width="63%">
Sets the reference rasterizer's race-condition tracking options for a specific shader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype">SetShaderTrackingOptionsByType</a>
</td>
<td align="left" width="63%">
Sets the reference rasterizer's default race-condition tracking options for the specified resource types.

</td>
</tr>
</table> 


## -remarks



To get this interface, turn on the <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a> and use <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a> from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-interfaces">Layer Interfaces</a>
 

 

