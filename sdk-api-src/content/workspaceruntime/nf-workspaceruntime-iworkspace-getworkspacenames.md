---
UID: NF:workspaceruntime.IWorkspace.GetWorkspaceNames
title: IWorkspace::GetWorkspaceNames (workspaceruntime.h)
description: Retrieves the names of the connections in the current process.
helpviewer_keywords: ["GetWorkspaceNames","GetWorkspaceNames method [Remote Desktop Services]","GetWorkspaceNames method [Remote Desktop Services]","IWorkspace interface","GetWorkspaceNames method [Remote Desktop Services]","IWorkspace2 interface","GetWorkspaceNames method [Remote Desktop Services]","IWorkspace3 interface","GetWorkspaceNames method [Remote Desktop Services]","Workspace object","IWorkspace interface [Remote Desktop Services]","GetWorkspaceNames method","IWorkspace.GetWorkspaceNames","IWorkspace2 interface [Remote Desktop Services]","GetWorkspaceNames method","IWorkspace2::GetWorkspaceNames","IWorkspace3 interface [Remote Desktop Services]","GetWorkspaceNames method","IWorkspace3::GetWorkspaceNames","IWorkspace::GetWorkspaceNames","Workspace object [Remote Desktop Services]","GetWorkspaceNames method","termserv.iworkspace_getworkspacenames","workspaceruntime/IWorkspace2::GetWorkspaceNames","workspaceruntime/IWorkspace3::GetWorkspaceNames","workspaceruntime/IWorkspace::GetWorkspaceNames"]
old-location: termserv\iworkspace_getworkspacenames.htm
tech.root: TermServ
ms.assetid: 379a9fb5-36e3-4c3d-a276-9d0804599b42
ms.date: 12/05/2018
ms.keywords: GetWorkspaceNames, GetWorkspaceNames method [Remote Desktop Services], GetWorkspaceNames method [Remote Desktop Services],IWorkspace interface, GetWorkspaceNames method [Remote Desktop Services],IWorkspace2 interface, GetWorkspaceNames method [Remote Desktop Services],IWorkspace3 interface, GetWorkspaceNames method [Remote Desktop Services],Workspace object, IWorkspace interface [Remote Desktop Services],GetWorkspaceNames method, IWorkspace.GetWorkspaceNames, IWorkspace2 interface [Remote Desktop Services],GetWorkspaceNames method, IWorkspace2::GetWorkspaceNames, IWorkspace3 interface [Remote Desktop Services],GetWorkspaceNames method, IWorkspace3::GetWorkspaceNames, IWorkspace::GetWorkspaceNames, Workspace object [Remote Desktop Services],GetWorkspaceNames method, termserv.iworkspace_getworkspacenames, workspaceruntime/IWorkspace2::GetWorkspaceNames, workspaceruntime/IWorkspace3::GetWorkspaceNames, workspaceruntime/IWorkspace::GetWorkspaceNames
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
 - IWorkspace::GetWorkspaceNames
 - workspaceruntime/IWorkspace::GetWorkspaceNames
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
 - IWorkspace.GetWorkspaceNames
 - IWorkspace2.GetWorkspaceNames
 - IWorkspace3.GetWorkspaceNames
 - Workspace.GetWorkspaceNames
---

# IWorkspace::GetWorkspaceNames


## -description

Retrieves the names of the connections in the current process.

## -parameters

### -param psaWkspNames [out]

A pointer to an array of <b>BSTR</b> variables to receive the names of the connections.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace">IWorkspace</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2">IWorkspace2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3">IWorkspace3</a>