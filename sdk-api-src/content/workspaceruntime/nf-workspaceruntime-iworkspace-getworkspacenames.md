---
UID: NF:workspaceruntime.IWorkspace.GetWorkspaceNames
title: IWorkspace::GetWorkspaceNames
author: windows-sdk-content
description: Retrieves the names of the connections in the current process.
old-location: termserv\iworkspace_getworkspacenames.htm
tech.root: termserv
ms.assetid: 379a9fb5-36e3-4c3d-a276-9d0804599b42
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetWorkspaceNames, GetWorkspaceNames method [Remote Desktop Services], GetWorkspaceNames method [Remote Desktop Services],IWorkspace interface, GetWorkspaceNames method [Remote Desktop Services],IWorkspace2 interface, GetWorkspaceNames method [Remote Desktop Services],IWorkspace3 interface, GetWorkspaceNames method [Remote Desktop Services],Workspace object, IWorkspace interface [Remote Desktop Services],GetWorkspaceNames method, IWorkspace.GetWorkspaceNames, IWorkspace2 interface [Remote Desktop Services],GetWorkspaceNames method, IWorkspace2::GetWorkspaceNames, IWorkspace3 interface [Remote Desktop Services],GetWorkspaceNames method, IWorkspace3::GetWorkspaceNames, IWorkspace::GetWorkspaceNames, Workspace object [Remote Desktop Services],GetWorkspaceNames method, termserv.iworkspace_getworkspacenames, workspaceruntime/IWorkspace2::GetWorkspaceNames, workspaceruntime/IWorkspace3::GetWorkspaceNames, workspaceruntime/IWorkspace::GetWorkspaceNames
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspace::GetWorkspaceNames


## -description


Retrieves the names of the connections in the current process.


## -parameters




### -param psaWkspNames [out]

A pointer to an array of <b>BSTR</b> variables to receive the names of the connections.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7a94ef42-8a63-4709-816d-1f51a948d486">IWorkspace</a>



<a href="https://msdn.microsoft.com/8155cd78-4c6b-47a9-a2c7-f9fffc95f700">IWorkspace2</a>



<a href="https://msdn.microsoft.com/a63240fb-8724-4cd2-b845-f48075f4cb57">IWorkspace3</a>
 

 

