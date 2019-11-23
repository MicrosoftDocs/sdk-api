---
UID: NN:workspaceruntime.IWorkspaceScriptable2
title: IWorkspaceScriptable2 (workspaceruntime.h)

description: Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.
old-location: termserv\iworkspacescriptable2.htm
tech.root: TermServ
ms.assetid: 66a6c283-bef9-4cb4-9035-d4a2d2cb7b4f

ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable2, IWorkspaceScriptable2 interface [Remote Desktop Services], IWorkspaceScriptable2 interface [Remote Desktop Services],described, termserv.iworkspacescriptable2, workspaceruntime/IWorkspaceScriptable2
ms.topic: interface
f1_keywords: 
 - "workspaceruntime/IWorkspaceScriptable2"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWorkspaceScriptable2 interface


## -description


Exposes methods that manage RemoteApp and Desktop Connection credentials and connections. This interface is implemented by the RemoteApp and Desktop Connection runtime. These methods are called by custom clients that implement the <a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceScriptable2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable">IWorkspaceScriptable</a>. <b>IWorkspaceScriptable2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacescriptable2-resourcedismissed">ResourceDismissed</a>
</td>
<td align="left" width="63%">
Alerts the user when a resource has been dismissed or is otherwise unavailable. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacescriptable2-startworkspaceex">StartWorkspaceEx</a>
</td>
<td align="left" width="63%">
Associates user credentials and certificates with a connection ID; also contains additional security and UI elements.

</td>
</tr>
</table> 

