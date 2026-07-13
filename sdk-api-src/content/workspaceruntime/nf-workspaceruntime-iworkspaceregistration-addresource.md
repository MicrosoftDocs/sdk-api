---
UID: NF:workspaceruntime.IWorkspaceRegistration.AddResource
title: IWorkspaceRegistration::AddResource (workspaceruntime.h)
description: Adds a resource to the connection in RemoteApp and Desktop Connection. (IWorkspaceRegistration2.AddResource)
helpviewer_keywords: ["AddResource","AddResource method [Remote Desktop Services]","AddResource method [Remote Desktop Services]","IWorkspaceRegistration interface","AddResource method [Remote Desktop Services]","IWorkspaceRegistration2 interface","AddResource method [Remote Desktop Services]","Workspace object","IWorkspaceRegistration interface [Remote Desktop Services]","AddResource method","IWorkspaceRegistration.AddResource","IWorkspaceRegistration2 interface [Remote Desktop Services]","AddResource method","IWorkspaceRegistration2::AddResource","IWorkspaceRegistration::AddResource","Workspace object [Remote Desktop Services]","AddResource method","termserv.iworkspaceregistration_addresource","workspaceruntime/IWorkspaceRegistration2::AddResource","workspaceruntime/IWorkspaceRegistration::AddResource"]
old-location: termserv\iworkspaceregistration_addresource.htm
tech.root: TermServ
ms.assetid: cd4ed8a0-e5a8-4809-a9bd-d013a84b0bd4
ms.date: 12/05/2018
ms.keywords: AddResource, AddResource method [Remote Desktop Services], AddResource method [Remote Desktop Services],IWorkspaceRegistration interface, AddResource method [Remote Desktop Services],IWorkspaceRegistration2 interface, AddResource method [Remote Desktop Services],Workspace object, IWorkspaceRegistration interface [Remote Desktop Services],AddResource method, IWorkspaceRegistration.AddResource, IWorkspaceRegistration2 interface [Remote Desktop Services],AddResource method, IWorkspaceRegistration2::AddResource, IWorkspaceRegistration::AddResource, Workspace object [Remote Desktop Services],AddResource method, termserv.iworkspaceregistration_addresource, workspaceruntime/IWorkspaceRegistration2::AddResource, workspaceruntime/IWorkspaceRegistration::AddResource
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
 - IWorkspaceRegistration::AddResource
 - workspaceruntime/IWorkspaceRegistration::AddResource
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
 - IWorkspaceRegistration.AddResource
 - IWorkspaceRegistration2.AddResource
 - Workspace.AddResource
---

# IWorkspaceRegistration::AddResource


## -description

Adds a resource to the connection in RemoteApp and Desktop Connection.

## -parameters

### -param pUnk [in]

A pointer to the <a href="/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a> object  that called this method.

### -param pdwCookie [out]

A pointer to a <b>DWORD</b> variable to receive the connection cookie for a new resource.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration">IWorkspaceRegistration</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2">IWorkspaceRegistration2</a>
