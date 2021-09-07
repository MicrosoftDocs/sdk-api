---
UID: NF:workspaceruntime.IWorkspace.GetProcessId
title: IWorkspace::GetProcessId (workspaceruntime.h)
description: Retrieves the process ID of the current connection in RemoteApp and Desktop Connection.
helpviewer_keywords: ["GetProcessId","GetProcessId method [Remote Desktop Services]","GetProcessId method [Remote Desktop Services]","IWorkspace interface","GetProcessId method [Remote Desktop Services]","IWorkspace2 interface","GetProcessId method [Remote Desktop Services]","IWorkspace3 interface","GetProcessId method [Remote Desktop Services]","Workspace object","IWorkspace interface [Remote Desktop Services]","GetProcessId method","IWorkspace.GetProcessId","IWorkspace2 interface [Remote Desktop Services]","GetProcessId method","IWorkspace2::GetProcessId","IWorkspace3 interface [Remote Desktop Services]","GetProcessId method","IWorkspace3::GetProcessId","IWorkspace::GetProcessId","Workspace object [Remote Desktop Services]","GetProcessId method","termserv.iworkspace_getprocessid","workspaceruntime/IWorkspace2::GetProcessId","workspaceruntime/IWorkspace3::GetProcessId","workspaceruntime/IWorkspace::GetProcessId"]
old-location: termserv\iworkspace_getprocessid.htm
tech.root: TermServ
ms.assetid: f703dfac-a896-472e-847c-cf44a96d9d9e
ms.date: 12/05/2018
ms.keywords: GetProcessId, GetProcessId method [Remote Desktop Services], GetProcessId method [Remote Desktop Services],IWorkspace interface, GetProcessId method [Remote Desktop Services],IWorkspace2 interface, GetProcessId method [Remote Desktop Services],IWorkspace3 interface, GetProcessId method [Remote Desktop Services],Workspace object, IWorkspace interface [Remote Desktop Services],GetProcessId method, IWorkspace.GetProcessId, IWorkspace2 interface [Remote Desktop Services],GetProcessId method, IWorkspace2::GetProcessId, IWorkspace3 interface [Remote Desktop Services],GetProcessId method, IWorkspace3::GetProcessId, IWorkspace::GetProcessId, Workspace object [Remote Desktop Services],GetProcessId method, termserv.iworkspace_getprocessid, workspaceruntime/IWorkspace2::GetProcessId, workspaceruntime/IWorkspace3::GetProcessId, workspaceruntime/IWorkspace::GetProcessId
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
 - IWorkspace::GetProcessId
 - workspaceruntime/IWorkspace::GetProcessId
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
 - IWorkspace.GetProcessId
 - IWorkspace2.GetProcessId
 - IWorkspace3.GetProcessId
 - Workspace.GetProcessId
---

# IWorkspace::GetProcessId


## -description

Retrieves the process ID of the current connection in RemoteApp and Desktop Connection.

## -parameters

### -param pulProcessId [out, retval]

A pointer to a <b>ULONG</b> variable to receive the process ID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace">IWorkspace</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2">IWorkspace2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3">IWorkspace3</a>