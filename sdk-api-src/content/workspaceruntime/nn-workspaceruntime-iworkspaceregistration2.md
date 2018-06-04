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

# IWorkspaceRegistration2 interface


## -description


Not implemented.

Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection. These methods are called by custom clients that implement the <a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceRegistration2</b> interface inherits from <a href="https://msdn.microsoft.com/29e7da7b-7da2-4000-8f3d-d12aa7e12fed">IWorkspaceRegistration</a>. <b>IWorkspaceRegistration2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspaceRegistration2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bb26842-ca30-40e2-b7a2-474dda4ad433">AddResourceEx</a>
</td>
<td align="left" width="63%">
Adds a resource to the connection in RemoteApp and Desktop Connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc8b7374-4a64-43a8-947e-0088aa26444e">RemoveResourceEx</a>
</td>
<td align="left" width="63%">
Notifies the RemoteApp and Desktop Connection runtime that  the client is disconnecting the connection.

</td>
</tr>
</table> 

