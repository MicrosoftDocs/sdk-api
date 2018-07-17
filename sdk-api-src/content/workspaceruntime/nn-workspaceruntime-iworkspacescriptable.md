---
UID: NN:workspaceruntime.IWorkspaceScriptable
title: IWorkspaceScriptable
author: windows-sdk-content
description: Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.
old-location: termserv\iworkspacescriptable.htm
old-project: termserv
ms.assetid: b6591369-d73f-4c7d-8525-428dffc9a341
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: IWorkspaceScriptable, IWorkspaceScriptable interface [Remote Desktop Services], IWorkspaceScriptable interface [Remote Desktop Services],described, termserv.iworkspacescriptable, workspaceruntime/IWorkspaceScriptable
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
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wksprt.exe
api_name:
 - IWorkspaceScriptable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceScriptable interface


## -description


Exposes methods that manage RemoteApp and Desktop Connection credentials and connections. This interface is implemented by the RemoteApp and Desktop Connection runtime. These methods are called by custom clients that implement the <a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceScriptable</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWorkspaceScriptable</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f21df395-3ff7-43c0-b1cd-010ae2c1d16b">ClearWorkspaceCredential</a>
</td>
<td align="left" width="63%">
Deletes the user credentials associated with the specified connection ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f422535a-0226-4951-b505-410711878fe7">DisconnectWorkspace</a>
</td>
<td align="left" width="63%">
Disconnects all existing connections associated with the specified connection ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9cf9c1a-8400-4a69-9cf1-0dfa6fe6a38b">DisconnectWorkspaceByFriendlyName</a>
</td>
<td align="left" width="63%">
Disconnects all existing connections associated with the connection that has the  specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b01f48d-161a-4cea-84d4-82c98d2e6998">IsWorkspaceCredentialSpecified</a>
</td>
<td align="left" width="63%">
Determines whether user credentials exist for the specified connection ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54608723-9a17-4bf2-a46d-8fed52378767">IsWorkspaceSSOEnabled</a>
</td>
<td align="left" width="63%">
Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4675fa5b-ea73-4046-a7f9-0b237bd283df">OnAuthenticated</a>
</td>
<td align="left" width="63%">
Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2985ae1-7874-43e8-b0d3-ef3f13ac2f8d">StartWorkspace</a>
</td>
<td align="left" width="63%">
Associates user credentials and certificates with a connection ID.

</td>
</tr>
</table> 

