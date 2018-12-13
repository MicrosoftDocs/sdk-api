---
UID: NN:workspaceruntime.IWorkspaceScriptable3
title: IWorkspaceScriptable3
author: windows-sdk-content
description: Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.
old-location: termserv\iworkspacescriptable3.htm
tech.root: TermServ
ms.assetid: 6fe02f0a-8cce-47f0-807e-e627336adf2c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWorkspaceScriptable3, IWorkspaceScriptable3 interface [Remote Desktop Services], IWorkspaceScriptable3 interface [Remote Desktop Services],described, termserv.iworkspacescriptable3, workspaceruntime/IWorkspaceScriptable3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: workspaceruntime.h
req.include-header: Workspaceruntime.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
 - IWorkspaceScriptable3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspaceScriptable3 interface


## -description


Not implemented.

Exposes methods that manage RemoteApp and Desktop Connection credentials and connections. This interface is implemented by the RemoteApp and Desktop Connection runtime. These methods are called by custom clients that implement the <a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceScriptable3</b> interface inherits from <a href="https://msdn.microsoft.com/66a6c283-bef9-4cb4-9035-d4a2d2cb7b4f">IWorkspaceScriptable2</a>. <b>IWorkspaceScriptable3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspaceScriptable3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/819eb47e-f697-4b34-a91f-44aa95cf116a">StartWorkspaceEx2</a>
</td>
<td align="left" width="63%">
Associates user credentials and certificates with a connection ID.

</td>
</tr>
</table> 

