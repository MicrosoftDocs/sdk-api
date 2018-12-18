---
UID: NN:workspaceruntime.IWorkspaceScriptable2
title: IWorkspaceScriptable2
author: windows-sdk-content
description: Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.
old-location: termserv\iworkspacescriptable2.htm
tech.root: TermServ
ms.assetid: 66a6c283-bef9-4cb4-9035-d4a2d2cb7b4f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWorkspaceScriptable2, IWorkspaceScriptable2 interface [Remote Desktop Services], IWorkspaceScriptable2 interface [Remote Desktop Services],described, termserv.iworkspacescriptable2, workspaceruntime/IWorkspaceScriptable2
ms.topic: interface
req.header: workspaceruntime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WorkspaceRuntime.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: WkspRt.exe
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WkspRt.exe
api_name:
 - IWorkspaceScriptable2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspaceScriptable2 interface


## -description


Exposes methods that manage RemoteApp and Desktop Connection credentials and connections. This interface is implemented by the RemoteApp and Desktop Connection runtime. These methods are called by custom clients that implement the <a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceScriptable2</b> interface inherits from <a href="https://msdn.microsoft.com/b6591369-d73f-4c7d-8525-428dffc9a341">IWorkspaceScriptable</a>. <b>IWorkspaceScriptable2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspaceScriptable2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e45d806c-56de-4f76-a76a-ba6db63f4ac2">ResourceDismissed</a>
</td>
<td align="left" width="63%">
Alerts the user when a resource has been dismissed or is otherwise unavailable. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8383ee1c-ff6a-4251-8b0d-a2a8c0674873">StartWorkspaceEx</a>
</td>
<td align="left" width="63%">
Associates user credentials and certificates with a connection ID; also contains additional security and UI elements.

</td>
</tr>
</table> 

