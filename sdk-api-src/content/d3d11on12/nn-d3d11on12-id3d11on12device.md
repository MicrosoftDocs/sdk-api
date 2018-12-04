---
UID: NN:d3d11on12.ID3D11On12Device
title: ID3D11On12Device
author: windows-sdk-content
description: Handles the creation, wrapping and releasing of D3D11 resources for Direct3D 11on12.
old-location: direct3d12\id3d11on12device.htm
tech.root: direct3d12
ms.assetid: 031F9AC2-E5C0-47F9-B084-2D2431F1187A
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ID3D11On12Device, ID3D11On12Device interface, ID3D11On12Device interface,described, d3d11on12/ID3D11On12Device, direct3d12.id3d11on12device
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11on12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - ID3D11On12Device
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11On12Device interface


## -description


Handles the creation, wrapping and releasing of D3D11 resources for Direct3D 11on12.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11On12Device</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11On12Device</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11On12Device</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/123FC8D9-6411-4CB7-921B-CEB32F5A9AD9">AcquireWrappedResources</a>
</td>
<td align="left" width="63%">
Acquires D3D11 resources for use with D3D 11on12.
          Indicates that rendering to the wrapped resources can begin again.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83B37B0A-9965-40F6-A5B1-8B4DC21BC455">CreateWrappedResource</a>
</td>
<td align="left" width="63%">
This method creates D3D11 resources for use with D3D 11on12.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6591D7D4-9B8D-4837-9DCF-0502CC26E725">ReleaseWrappedResources</a>
</td>
<td align="left" width="63%">
Releases D3D11 resources that were wrapped for D3D 11on12.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/861D89C4-59D1-43BF-9791-375DD1577716">11on12 Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

