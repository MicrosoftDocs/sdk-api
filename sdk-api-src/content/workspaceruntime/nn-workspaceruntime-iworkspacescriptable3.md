---
UID: NN:workspaceruntime.IWorkspaceScriptable3
title: IWorkspaceScriptable3 (workspaceruntime.h)
description: Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.
helpviewer_keywords: ["IWorkspaceScriptable3","IWorkspaceScriptable3 interface [Remote Desktop Services]","IWorkspaceScriptable3 interface [Remote Desktop Services]","described","termserv.iworkspacescriptable3","workspaceruntime/IWorkspaceScriptable3"]
old-location: termserv\iworkspacescriptable3.htm
tech.root: TermServ
ms.assetid: 6fe02f0a-8cce-47f0-807e-e627336adf2c
ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable3, IWorkspaceScriptable3 interface [Remote Desktop Services], IWorkspaceScriptable3 interface [Remote Desktop Services],described, termserv.iworkspacescriptable3, workspaceruntime/IWorkspaceScriptable3
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWorkspaceScriptable3
 - workspaceruntime/IWorkspaceScriptable3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WkspRt.exe
api_name:
 - IWorkspaceScriptable3
---

# IWorkspaceScriptable3 interface


## -description

Not implemented.

Exposes methods that manage RemoteApp and Desktop Connection credentials and connections. This interface is implemented by the RemoteApp and Desktop Connection runtime. These methods are called by custom clients that implement the <a href="/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceScriptable3</b> interface inherits from <a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2">IWorkspaceScriptable2</a>. <b>IWorkspaceScriptable3</b> also has these types of members:
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
<a href="/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacescriptable3-startworkspaceex2">StartWorkspaceEx2</a>
</td>
<td align="left" width="63%">
Associates user credentials and certificates with a connection ID.

</td>
</tr>
</table>