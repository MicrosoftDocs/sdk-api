---
UID: NN:workspaceruntimeclientext.IWorkspaceClientExt
title: IWorkspaceClientExt (workspaceruntimeclientext.h)
author: windows-sdk-content
description: Exposes methods that allow the runtime to disconnect a custom client in RemoteApp and Desktop Connection.
old-location: termserv\iworkspaceclientext.htm
tech.root: TermServ
ms.assetid: f72b0709-1a55-49c9-ab5d-22f9259c41f0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWorkspaceClientExt, IWorkspaceClientExt interface [Remote Desktop Services], IWorkspaceClientExt interface [Remote Desktop Services],described, termserv.iworkspaceclientext, workspaceruntimeclientext/IWorkspaceClientExt
ms.topic: interface
req.header: workspaceruntimeclientext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Workspaceruntimeclientext.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Workspaceruntimeclientext.h
api_name:
 - IWorkspaceClientExt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspaceClientExt interface


## -description


Exposes methods that allow the runtime to disconnect a custom client in RemoteApp and Desktop Connection.  This interface is the outbound interface of the custom client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceClientExt</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWorkspaceClientExt</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspaceClientExt</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f67fa6f3-621a-4015-8fcf-85b1302a3c8a">GetResourceDisplayName</a>
</td>
<td align="left" width="63%">
Returns the display name of the custom client in RemoteApp and Desktop Connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7a0c77c-0579-48dd-bc06-8ffe48358661">GetResourceId</a>
</td>
<td align="left" width="63%">
Returns the ID of the custom client in RemoteApp and Desktop Connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07c2546b-e9bf-46e6-a1de-6da31fa1579b">IssueDisconnect</a>
</td>
<td align="left" width="63%">
Disconnects the custom client in RemoteApp and Desktop Connection.

</td>
</tr>
</table> 

