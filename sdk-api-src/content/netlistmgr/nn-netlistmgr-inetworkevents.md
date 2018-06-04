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

# INetworkEvents interface


## -description


<b>INetworkEvents</b> is a notification sink interface that a client implements to get network related events. These APIs are all callback functions that are called automatically when the respective events are raised.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetworkEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INetworkEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetworkEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fda364e-ad6a-447a-ba0c-25e5d52ef5c5">NetworkAdded</a>
</td>
<td align="left" width="63%">
Called when a new network is added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adaf3abe-9a8c-45af-bcc7-bcc516ed75ff">NetworkConnectivityChanged</a>
</td>
<td align="left" width="63%">
Called when network connectivity related changes occur. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae54cc29-6da8-405d-92f9-654239150dd0">NetworkDeleted</a>
</td>
<td align="left" width="63%">
Called when a network is deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a84f49ee-9efd-450e-a6e6-3f140330a9d0">NetworkPropertyChanged</a>
</td>
<td align="left" width="63%">
Called when a network property change is detected.

</td>
</tr>
</table> 

