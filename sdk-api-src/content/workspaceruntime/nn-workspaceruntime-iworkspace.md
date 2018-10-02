---
UID: NN:workspaceruntime.IWorkspace
title: IWorkspace
author: windows-sdk-content
description: Exposes methods that provide information about a connection in RemoteApp and Desktop Connection.
old-location: termserv\iworkspace.htm
tech.root: TermServ
ms.assetid: 7a94ef42-8a63-4709-816d-1f51a948d486
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWorkspace, IWorkspace interface [Remote Desktop Services], IWorkspace interface [Remote Desktop Services],described, termserv.iworkspace, workspaceruntime/IWorkspace
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
 - IWorkspace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspace interface


## -description


Exposes methods that provide information about a connection in RemoteApp and Desktop Connection. This interface is implemented by the Remote Desktop Services workspace runtime. These methods are called by custom clients that implement the <a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspace</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWorkspace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f703dfac-a896-472e-847c-cf44a96d9d9e">GetProcessId</a>
</td>
<td align="left" width="63%">
Retrieves the process ID of the current connection in RemoteApp and Desktop Connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/379a9fb5-36e3-4c3d-a276-9d0804599b42">GetWorkspaceNames</a>
</td>
<td align="left" width="63%">
Retrieves the names of the connections in the current process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1d7e0c2-90bc-49c9-b7d5-380e13af4bba">StartRemoteApplication</a>
</td>
<td align="left" width="63%">
Starts a RemoteApp program.

</td>
</tr>
</table> 

