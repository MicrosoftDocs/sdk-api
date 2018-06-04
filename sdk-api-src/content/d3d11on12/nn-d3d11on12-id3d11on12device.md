---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

