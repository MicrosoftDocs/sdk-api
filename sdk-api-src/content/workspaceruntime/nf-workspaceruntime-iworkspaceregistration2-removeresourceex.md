---
UID: NF:workspaceruntime.IWorkspaceRegistration2.RemoveResourceEx
title: IWorkspaceRegistration2::RemoveResourceEx (workspaceruntime.h)
description: Notifies the RemoteApp and Desktop Connection runtime that the client is disconnecting the connection. (IWorkspaceRegistration2::RemoveResourceEx)
helpviewer_keywords: ["IWorkspaceRegistration2 interface [Remote Desktop Services]","RemoveResourceEx method","IWorkspaceRegistration2.RemoveResourceEx","IWorkspaceRegistration2::RemoveResourceEx","RemoveResourceEx","RemoveResourceEx method [Remote Desktop Services]","RemoveResourceEx method [Remote Desktop Services]","IWorkspaceRegistration2 interface","RemoveResourceEx method [Remote Desktop Services]","Workspace object","Workspace object [Remote Desktop Services]","RemoveResourceEx method","termserv.iworkspaceregistration2_removeresourceex","workspaceruntime/IWorkspaceRegistration2::RemoveResourceEx"]
old-location: termserv\iworkspaceregistration2_removeresourceex.htm
tech.root: TermServ
ms.assetid: dc8b7374-4a64-43a8-947e-0088aa26444e
ms.date: 12/05/2018
ms.keywords: IWorkspaceRegistration2 interface [Remote Desktop Services],RemoveResourceEx method, IWorkspaceRegistration2.RemoveResourceEx, IWorkspaceRegistration2::RemoveResourceEx, RemoveResourceEx, RemoveResourceEx method [Remote Desktop Services], RemoveResourceEx method [Remote Desktop Services],IWorkspaceRegistration2 interface, RemoveResourceEx method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],RemoveResourceEx method, termserv.iworkspaceregistration2_removeresourceex, workspaceruntime/IWorkspaceRegistration2::RemoveResourceEx
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
 - IWorkspaceRegistration2::RemoveResourceEx
 - workspaceruntime/IWorkspaceRegistration2::RemoveResourceEx
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - IWorkspaceRegistration2::RemoveResourceEx
---

# IWorkspaceRegistration2::RemoveResourceEx


## -description

Not implemented.

Notifies the RemoteApp and Desktop Connection runtime that  the client is disconnecting the connection.

## -parameters

### -param dwCookieConnection [in]

A <b>DWORD</b> value that contains a connection cookie returned by the <a href="/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspaceregistration2-addresourceex">AddResourceEx</a> method.

### -param correlationId [in]

TBD

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2">IWorkspaceRegistration2</a>
