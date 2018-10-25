---
UID: NN:workspaceruntime.IWorkspaceRegistration
title: IWorkspaceRegistration
author: windows-sdk-content
description: Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.
old-location: termserv\iworkspaceregistration.htm
tech.root: termserv
ms.assetid: 29e7da7b-7da2-4000-8f3d-d12aa7e12fed
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IWorkspaceRegistration, IWorkspaceRegistration interface [Remote Desktop Services], IWorkspaceRegistration interface [Remote Desktop Services],described, termserv.iworkspaceregistration, workspaceruntime/IWorkspaceRegistration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: workspaceruntime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WorkspaceRuntime.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wksprt.exe
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wksprt.exe
api_name:
 - IWorkspaceRegistration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspaceRegistration interface


## -description


Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection. These methods are called by custom clients that implement the <a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceRegistration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWorkspaceRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspaceRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd4ed8a0-e5a8-4809-a9bd-d013a84b0bd4">AddResource</a>
</td>
<td align="left" width="63%">
Adds a resource to the connection in RemoteApp and Desktop Connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f700e3c2-06fe-4f98-9b1e-aeadc339ed7a">RemoveResource</a>
</td>
<td align="left" width="63%">
Notifies the RemoteApp and Desktop Connection runtime that  the client is disconnecting the connection.

</td>
</tr>
</table> 

