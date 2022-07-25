---
UID: NF:workspaceruntime.IWorkspaceScriptable.DisconnectWorkspace
title: IWorkspaceScriptable::DisconnectWorkspace (workspaceruntime.h)
description: Disconnects all existing connections associated with the specified connection ID.
helpviewer_keywords: ["DisconnectWorkspace","DisconnectWorkspace method [Remote Desktop Services]","DisconnectWorkspace method [Remote Desktop Services]","IWorkspaceScriptable interface","DisconnectWorkspace method [Remote Desktop Services]","IWorkspaceScriptable2 interface","DisconnectWorkspace method [Remote Desktop Services]","IWorkspaceScriptable3 interface","DisconnectWorkspace method [Remote Desktop Services]","Workspace object","IWorkspaceScriptable interface [Remote Desktop Services]","DisconnectWorkspace method","IWorkspaceScriptable.DisconnectWorkspace","IWorkspaceScriptable2 interface [Remote Desktop Services]","DisconnectWorkspace method","IWorkspaceScriptable2::DisconnectWorkspace","IWorkspaceScriptable3 interface [Remote Desktop Services]","DisconnectWorkspace method","IWorkspaceScriptable3::DisconnectWorkspace","IWorkspaceScriptable::DisconnectWorkspace","Workspace object [Remote Desktop Services]","DisconnectWorkspace method","termserv.iworkspacescriptable_disconnectworkspace","workspaceruntime/IWorkspaceScriptable2::DisconnectWorkspace","workspaceruntime/IWorkspaceScriptable3::DisconnectWorkspace","workspaceruntime/IWorkspaceScriptable::DisconnectWorkspace"]
old-location: termserv\iworkspacescriptable_disconnectworkspace.htm
tech.root: TermServ
ms.assetid: f422535a-0226-4951-b505-410711878fe7
ms.date: 12/05/2018
ms.keywords: DisconnectWorkspace, DisconnectWorkspace method [Remote Desktop Services], DisconnectWorkspace method [Remote Desktop Services],IWorkspaceScriptable interface, DisconnectWorkspace method [Remote Desktop Services],IWorkspaceScriptable2 interface, DisconnectWorkspace method [Remote Desktop Services],IWorkspaceScriptable3 interface, DisconnectWorkspace method [Remote Desktop Services],Workspace object, IWorkspaceScriptable interface [Remote Desktop Services],DisconnectWorkspace method, IWorkspaceScriptable.DisconnectWorkspace, IWorkspaceScriptable2 interface [Remote Desktop Services],DisconnectWorkspace method, IWorkspaceScriptable2::DisconnectWorkspace, IWorkspaceScriptable3 interface [Remote Desktop Services],DisconnectWorkspace method, IWorkspaceScriptable3::DisconnectWorkspace, IWorkspaceScriptable::DisconnectWorkspace, Workspace object [Remote Desktop Services],DisconnectWorkspace method, termserv.iworkspacescriptable_disconnectworkspace, workspaceruntime/IWorkspaceScriptable2::DisconnectWorkspace, workspaceruntime/IWorkspaceScriptable3::DisconnectWorkspace, workspaceruntime/IWorkspaceScriptable::DisconnectWorkspace
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
 - IWorkspaceScriptable::DisconnectWorkspace
 - workspaceruntime/IWorkspaceScriptable::DisconnectWorkspace
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
 - IWorkspaceScriptable.DisconnectWorkspace
 - IWorkspaceScriptable2.DisconnectWorkspace
 - IWorkspaceScriptable3.DisconnectWorkspace
 - Workspace.DisconnectWorkspace
---

# IWorkspaceScriptable::DisconnectWorkspace


## -description

Disconnects all existing connections associated with the specified connection ID. It also deletes the corresponding entries from the credential store.

## -parameters

### -param bstrWorkspaceId [in]

A string that contains the connection ID of the connection to disconnect.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable">IWorkspaceScriptable</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2">IWorkspaceScriptable2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3">IWorkspaceScriptable3</a>