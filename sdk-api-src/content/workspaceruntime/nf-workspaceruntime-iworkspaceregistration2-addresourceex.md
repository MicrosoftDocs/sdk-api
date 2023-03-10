---
UID: NF:workspaceruntime.IWorkspaceRegistration2.AddResourceEx
title: IWorkspaceRegistration2::AddResourceEx (workspaceruntime.h)
description: Adds a resource to the connection in RemoteApp and Desktop Connection. (IWorkspaceRegistration2::AddResourceEx)
helpviewer_keywords: ["AddResourceEx","AddResourceEx method [Remote Desktop Services]","AddResourceEx method [Remote Desktop Services]","IWorkspaceRegistration2 interface","AddResourceEx method [Remote Desktop Services]","Workspace object","IWorkspaceRegistration2 interface [Remote Desktop Services]","AddResourceEx method","IWorkspaceRegistration2.AddResourceEx","IWorkspaceRegistration2::AddResourceEx","Workspace object [Remote Desktop Services]","AddResourceEx method","termserv.iworkspaceregistration2_addresourceex","workspaceruntime/IWorkspaceRegistration2::AddResourceEx"]
old-location: termserv\iworkspaceregistration2_addresourceex.htm
tech.root: TermServ
ms.assetid: 7bb26842-ca30-40e2-b7a2-474dda4ad433
ms.date: 12/05/2018
ms.keywords: AddResourceEx, AddResourceEx method [Remote Desktop Services], AddResourceEx method [Remote Desktop Services],IWorkspaceRegistration2 interface, AddResourceEx method [Remote Desktop Services],Workspace object, IWorkspaceRegistration2 interface [Remote Desktop Services],AddResourceEx method, IWorkspaceRegistration2.AddResourceEx, IWorkspaceRegistration2::AddResourceEx, Workspace object [Remote Desktop Services],AddResourceEx method, termserv.iworkspaceregistration2_addresourceex, workspaceruntime/IWorkspaceRegistration2::AddResourceEx
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
 - IWorkspaceRegistration2::AddResourceEx
 - workspaceruntime/IWorkspaceRegistration2::AddResourceEx
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - IWorkspaceRegistration2::AddResourceEx
---

# IWorkspaceRegistration2::AddResourceEx


## -description

Not implemented.

Adds a resource to the connection in RemoteApp and Desktop Connection.

## -parameters

### -param pUnk [in]

A pointer to the <a href="/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a> object  that called this method.

### -param bstrEventLogUploadAddress [in]

TBD

### -param pdwCookie [out]

A pointer to a <b>DWORD</b> variable to receive the connection cookie for a new resource.

### -param correlationId [in]

TBD

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2">IWorkspaceRegistration2</a>
