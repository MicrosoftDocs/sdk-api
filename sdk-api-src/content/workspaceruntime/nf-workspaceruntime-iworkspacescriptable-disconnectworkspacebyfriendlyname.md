---
UID: NF:workspaceruntime.IWorkspaceScriptable.DisconnectWorkspaceByFriendlyName
title: IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName (workspaceruntime.h)
description: Disconnects all existing connections associated with the connection that has the specified name.
helpviewer_keywords: ["DisconnectWorkspaceByFriendlyName","DisconnectWorkspaceByFriendlyName method [Remote Desktop Services]","DisconnectWorkspaceByFriendlyName method [Remote Desktop Services]","IWorkspaceScriptable interface","DisconnectWorkspaceByFriendlyName method [Remote Desktop Services]","IWorkspaceScriptable2 interface","DisconnectWorkspaceByFriendlyName method [Remote Desktop Services]","IWorkspaceScriptable3 interface","DisconnectWorkspaceByFriendlyName method [Remote Desktop Services]","Workspace object","IWorkspaceScriptable interface [Remote Desktop Services]","DisconnectWorkspaceByFriendlyName method","IWorkspaceScriptable.DisconnectWorkspaceByFriendlyName","IWorkspaceScriptable2 interface [Remote Desktop Services]","DisconnectWorkspaceByFriendlyName method","IWorkspaceScriptable2::DisconnectWorkspaceByFriendlyName","IWorkspaceScriptable3 interface [Remote Desktop Services]","DisconnectWorkspaceByFriendlyName method","IWorkspaceScriptable3::DisconnectWorkspaceByFriendlyName","IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName","Workspace object [Remote Desktop Services]","DisconnectWorkspaceByFriendlyName method","termserv.iworkspacescriptable_disconnectworkspacebyfriendlyname","workspaceruntime/IWorkspaceScriptable2::DisconnectWorkspaceByFriendlyName","workspaceruntime/IWorkspaceScriptable3::DisconnectWorkspaceByFriendlyName","workspaceruntime/IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName"]
old-location: termserv\iworkspacescriptable_disconnectworkspacebyfriendlyname.htm
tech.root: TermServ
ms.assetid: e9cf9c1a-8400-4a69-9cf1-0dfa6fe6a38b
ms.date: 12/05/2018
ms.keywords: DisconnectWorkspaceByFriendlyName, DisconnectWorkspaceByFriendlyName method [Remote Desktop Services], DisconnectWorkspaceByFriendlyName method [Remote Desktop Services],IWorkspaceScriptable interface, DisconnectWorkspaceByFriendlyName method [Remote Desktop Services],IWorkspaceScriptable2 interface, DisconnectWorkspaceByFriendlyName method [Remote Desktop Services],IWorkspaceScriptable3 interface, DisconnectWorkspaceByFriendlyName method [Remote Desktop Services],Workspace object, IWorkspaceScriptable interface [Remote Desktop Services],DisconnectWorkspaceByFriendlyName method, IWorkspaceScriptable.DisconnectWorkspaceByFriendlyName, IWorkspaceScriptable2 interface [Remote Desktop Services],DisconnectWorkspaceByFriendlyName method, IWorkspaceScriptable2::DisconnectWorkspaceByFriendlyName, IWorkspaceScriptable3 interface [Remote Desktop Services],DisconnectWorkspaceByFriendlyName method, IWorkspaceScriptable3::DisconnectWorkspaceByFriendlyName, IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName, Workspace object [Remote Desktop Services],DisconnectWorkspaceByFriendlyName method, termserv.iworkspacescriptable_disconnectworkspacebyfriendlyname, workspaceruntime/IWorkspaceScriptable2::DisconnectWorkspaceByFriendlyName, workspaceruntime/IWorkspaceScriptable3::DisconnectWorkspaceByFriendlyName, workspaceruntime/IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName
 - workspaceruntime/IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wksprt.exe
api_name:
 - IWorkspaceScriptable.DisconnectWorkspaceByFriendlyName
 - IWorkspaceScriptable2.DisconnectWorkspaceByFriendlyName
 - IWorkspaceScriptable3.DisconnectWorkspaceByFriendlyName
 - Workspace.DisconnectWorkspaceByFriendlyName
---

# IWorkspaceScriptable::DisconnectWorkspaceByFriendlyName


## -description

Disconnects all existing connections associated with the connection that has the  specified name. It also deletes the corresponding entries from the RemoteApp and Desktop Connection store.

## -parameters

### -param bstrWorkspaceFriendlyName [in]

A string that contains the friendly name of the connection to disconnect.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable">IWorkspaceScriptable</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2">IWorkspaceScriptable2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3">IWorkspaceScriptable3</a>