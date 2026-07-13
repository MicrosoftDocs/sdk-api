---
UID: NF:workspaceruntime.IWorkspaceRegistration.RemoveResource
title: IWorkspaceRegistration::RemoveResource (workspaceruntime.h)
description: Notifies the RemoteApp and Desktop Connection runtime that the client is disconnecting the connection. (IWorkspaceRegistration2.RemoveResource)
helpviewer_keywords: ["IWorkspaceRegistration interface [Remote Desktop Services]","RemoveResource method","IWorkspaceRegistration.RemoveResource","IWorkspaceRegistration2 interface [Remote Desktop Services]","RemoveResource method","IWorkspaceRegistration2::RemoveResource","IWorkspaceRegistration::RemoveResource","RemoveResource","RemoveResource method [Remote Desktop Services]","RemoveResource method [Remote Desktop Services]","IWorkspaceRegistration interface","RemoveResource method [Remote Desktop Services]","IWorkspaceRegistration2 interface","RemoveResource method [Remote Desktop Services]","Workspace object","Workspace object [Remote Desktop Services]","RemoveResource method","termserv.iworkspaceregistration_removeresource","workspaceruntime/IWorkspaceRegistration2::RemoveResource","workspaceruntime/IWorkspaceRegistration::RemoveResource"]
old-location: termserv\iworkspaceregistration_removeresource.htm
tech.root: TermServ
ms.assetid: f700e3c2-06fe-4f98-9b1e-aeadc339ed7a
ms.date: 12/05/2018
ms.keywords: IWorkspaceRegistration interface [Remote Desktop Services],RemoveResource method, IWorkspaceRegistration.RemoveResource, IWorkspaceRegistration2 interface [Remote Desktop Services],RemoveResource method, IWorkspaceRegistration2::RemoveResource, IWorkspaceRegistration::RemoveResource, RemoveResource, RemoveResource method [Remote Desktop Services], RemoveResource method [Remote Desktop Services],IWorkspaceRegistration interface, RemoveResource method [Remote Desktop Services],IWorkspaceRegistration2 interface, RemoveResource method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],RemoveResource method, termserv.iworkspaceregistration_removeresource, workspaceruntime/IWorkspaceRegistration2::RemoveResource, workspaceruntime/IWorkspaceRegistration::RemoveResource
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
 - IWorkspaceRegistration::RemoveResource
 - workspaceruntime/IWorkspaceRegistration::RemoveResource
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
 - IWorkspaceRegistration.RemoveResource
 - IWorkspaceRegistration2.RemoveResource
 - Workspace.RemoveResource
---

# IWorkspaceRegistration::RemoveResource


## -description

Notifies the RemoteApp and Desktop Connection runtime that  the client is disconnecting the connection.

## -parameters

### -param dwCookieConnection [in]

A <b>DWORD</b> value that contains a connection cookie returned by the <a href="/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspaceregistration-addresource">AddResource</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration">IWorkspaceRegistration</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2">IWorkspaceRegistration2</a>
