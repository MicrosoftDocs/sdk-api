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

# ItsPubPlugin2 interface


## -description


Specifies methods that provide information about resources available to users of RemoteApp and Desktop Connections. This interface is an enhancement to the <a href="https://msdn.microsoft.com/37d33f27-a811-4c97-bc80-ff8a5b8fcb7c">ItsPubPlugin</a> interface.

The methods in this interface are called by the RemoteApp and Desktop Connection Management service in Remote Desktop Web Access (RD Web Access) and Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ItsPubPlugin2</b> interface inherits from <a href="https://msdn.microsoft.com/37d33f27-a811-4c97-bc80-ff8a5b8fcb7c">ItsPubPlugin</a>. <b>ItsPubPlugin2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ItsPubPlugin2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/962d7de7-a447-44f9-b3bd-a87d122a6328">DeletePersonalDesktopAssignment</a>
</td>
<td align="left" width="63%">
Called to delete a mapping between the specified user and a virtual machine in a personal virtual desktop collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8edb3f28-0796-478e-bf0a-b157e1e12dc2">GetResource2</a>
</td>
<td align="left" width="63%">
This method is reserved and should always return <b>E_NOTIMPL</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58b30088-be32-4aa0-88a4-459df52db7af">GetResource2List</a>
</td>
<td align="left" width="63%">
Retrieves a list of resources assigned to the specified user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f88d7a6-c662-4a14-a288-9c346c8fb7f1">ResolvePersonalDesktop</a>
</td>
<td align="left" width="63%">
Called to resolve a mapping between the specified user and a virtual machine in a personal virtual desktop collection.

</td>
</tr>
</table> 

