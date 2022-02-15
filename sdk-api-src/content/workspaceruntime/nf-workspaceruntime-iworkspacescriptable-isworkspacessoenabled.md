---
UID: NF:workspaceruntime.IWorkspaceScriptable.IsWorkspaceSSOEnabled
title: IWorkspaceScriptable::IsWorkspaceSSOEnabled (workspaceruntime.h)
description: Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.
helpviewer_keywords: ["IWorkspaceScriptable interface [Remote Desktop Services]","IsWorkspaceSSOEnabled method","IWorkspaceScriptable.IsWorkspaceSSOEnabled","IWorkspaceScriptable2 interface [Remote Desktop Services]","IsWorkspaceSSOEnabled method","IWorkspaceScriptable2::IsWorkspaceSSOEnabled","IWorkspaceScriptable3 interface [Remote Desktop Services]","IsWorkspaceSSOEnabled method","IWorkspaceScriptable3::IsWorkspaceSSOEnabled","IWorkspaceScriptable::IsWorkspaceSSOEnabled","IsWorkspaceSSOEnabled","IsWorkspaceSSOEnabled method [Remote Desktop Services]","IsWorkspaceSSOEnabled method [Remote Desktop Services]","IWorkspaceScriptable interface","IsWorkspaceSSOEnabled method [Remote Desktop Services]","IWorkspaceScriptable2 interface","IsWorkspaceSSOEnabled method [Remote Desktop Services]","IWorkspaceScriptable3 interface","IsWorkspaceSSOEnabled method [Remote Desktop Services]","Workspace object","Workspace object [Remote Desktop Services]","IsWorkspaceSSOEnabled method","termserv.iworkspacescriptable_isworkspacessoenabled","workspaceruntime/IWorkspaceScriptable2::IsWorkspaceSSOEnabled","workspaceruntime/IWorkspaceScriptable3::IsWorkspaceSSOEnabled","workspaceruntime/IWorkspaceScriptable::IsWorkspaceSSOEnabled"]
old-location: termserv\iworkspacescriptable_isworkspacessoenabled.htm
tech.root: TermServ
ms.assetid: 54608723-9a17-4bf2-a46d-8fed52378767
ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable interface [Remote Desktop Services],IsWorkspaceSSOEnabled method, IWorkspaceScriptable.IsWorkspaceSSOEnabled, IWorkspaceScriptable2 interface [Remote Desktop Services],IsWorkspaceSSOEnabled method, IWorkspaceScriptable2::IsWorkspaceSSOEnabled, IWorkspaceScriptable3 interface [Remote Desktop Services],IsWorkspaceSSOEnabled method, IWorkspaceScriptable3::IsWorkspaceSSOEnabled, IWorkspaceScriptable::IsWorkspaceSSOEnabled, IsWorkspaceSSOEnabled, IsWorkspaceSSOEnabled method [Remote Desktop Services], IsWorkspaceSSOEnabled method [Remote Desktop Services],IWorkspaceScriptable interface, IsWorkspaceSSOEnabled method [Remote Desktop Services],IWorkspaceScriptable2 interface, IsWorkspaceSSOEnabled method [Remote Desktop Services],IWorkspaceScriptable3 interface, IsWorkspaceSSOEnabled method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],IsWorkspaceSSOEnabled method, termserv.iworkspacescriptable_isworkspacessoenabled, workspaceruntime/IWorkspaceScriptable2::IsWorkspaceSSOEnabled, workspaceruntime/IWorkspaceScriptable3::IsWorkspaceSSOEnabled, workspaceruntime/IWorkspaceScriptable::IsWorkspaceSSOEnabled
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
 - IWorkspaceScriptable::IsWorkspaceSSOEnabled
 - workspaceruntime/IWorkspaceScriptable::IsWorkspaceSSOEnabled
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
 - IWorkspaceScriptable.IsWorkspaceSSOEnabled
 - IWorkspaceScriptable2.IsWorkspaceSSOEnabled
 - IWorkspaceScriptable3.IsWorkspaceSSOEnabled
 - Workspace.IsWorkspaceSSOEnabled
---

# IWorkspaceScriptable::IsWorkspaceSSOEnabled


## -description

Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.

## -parameters

### -param pbSSOEnabled [out, retval]

A pointer to a <b>VARIANT_BOOL</b> variable to receive  whether SSO is enabled. This value is <b>VARIANT_TRUE</b> if SSO is enabled; otherwise, <b>VARIANT_FALSE</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable">IWorkspaceScriptable</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2">IWorkspaceScriptable2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3">IWorkspaceScriptable3</a>