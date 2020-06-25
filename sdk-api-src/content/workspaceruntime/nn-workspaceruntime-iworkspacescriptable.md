---
UID: NN:workspaceruntime.IWorkspaceScriptable
title: IWorkspaceScriptable (workspaceruntime.h)
description: Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.
helpviewer_keywords: ["IWorkspaceScriptable","IWorkspaceScriptable interface [Remote Desktop Services]","IWorkspaceScriptable interface [Remote Desktop Services]","described","termserv.iworkspacescriptable","workspaceruntime/IWorkspaceScriptable"]
old-location: termserv\iworkspacescriptable.htm
tech.root: TermServ
ms.assetid: b6591369-d73f-4c7d-8525-428dffc9a341
ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable, IWorkspaceScriptable interface [Remote Desktop Services], IWorkspaceScriptable interface [Remote Desktop Services],described, termserv.iworkspacescriptable, workspaceruntime/IWorkspaceScriptable
f1_keywords:
- workspaceruntime/IWorkspaceScriptable
dev_langs:
- c++
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
- IWorkspaceScriptable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWorkspaceScriptable interface


## -description


Exposes methods that manage RemoteApp and Desktop Connection credentials and connections. This interface is implemented by the RemoteApp and Desktop Connection runtime. These methods are called by custom clients that implement the <a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceScriptable</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWorkspaceScriptable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspaceScriptable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacescriptable-clearworkspacecredential">ClearWorkspaceCredential</a>
</td>
<td align="left" width="63%">
Deletes the user credentials associated with the specified connection ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacescriptable-disconnectworkspace">DisconnectWorkspace</a>
</td>
<td align="left" width="63%">
Disconnects all existing connections associated with the specified connection ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacescriptable-disconnectworkspacebyfriendlyname">DisconnectWorkspaceByFriendlyName</a>
</td>
<td align="left" width="63%">
Disconnects all existing connections associated with the connection that has the  specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacescriptable-isworkspacecredentialspecified">IsWorkspaceCredentialSpecified</a>
</td>
<td align="left" width="63%">
Determines whether user credentials exist for the specified connection ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacescriptable-isworkspacessoenabled">IsWorkspaceSSOEnabled</a>
</td>
<td align="left" width="63%">
Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacescriptable-onauthenticated">OnAuthenticated</a>
</td>
<td align="left" width="63%">
Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspacescriptable-startworkspace">StartWorkspace</a>
</td>
<td align="left" width="63%">
Associates user credentials and certificates with a connection ID.

</td>
</tr>
</table> 

