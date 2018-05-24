---
UID: NF:workspaceruntime.IWorkspaceRegistration.AddResource
title: IWorkspaceRegistration::AddResource
author: windows-driver-content
description: Adds a resource to the connection in RemoteApp and Desktop Connection.
old-location: termserv\iworkspaceregistration_addresource.htm
old-project: TermServ
ms.assetid: cd4ed8a0-e5a8-4809-a9bd-d013a84b0bd4
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AddResource, AddResource method [Remote Desktop Services], AddResource method [Remote Desktop Services],IWorkspaceRegistration interface, AddResource method [Remote Desktop Services],IWorkspaceRegistration2 interface, AddResource method [Remote Desktop Services],Workspace object, IWorkspaceRegistration interface [Remote Desktop Services],AddResource method, IWorkspaceRegistration.AddResource, IWorkspaceRegistration2 interface [Remote Desktop Services],AddResource method, IWorkspaceRegistration2::AddResource, IWorkspaceRegistration::AddResource, Workspace object [Remote Desktop Services],AddResource method, termserv.iworkspaceregistration_addresource, workspaceruntime/IWorkspaceRegistration2::AddResource, workspaceruntime/IWorkspaceRegistration::AddResource
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
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wksprt.exe
api_name:
-	IWorkspaceRegistration.AddResource
-	IWorkspaceRegistration2.AddResource
-	Workspace.AddResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceRegistration::AddResource


## -description


Adds a resource to the connection in RemoteApp and Desktop Connection.


## -parameters




### -param pUnk [in]

A pointer to the <a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a> object  that called this method.


### -param pdwCookie [out]

A pointer to a <b>DWORD</b> variable to receive the connection cookie for a new resource.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/29e7da7b-7da2-4000-8f3d-d12aa7e12fed">IWorkspaceRegistration</a>



<a href="https://msdn.microsoft.com/b677863a-c8cc-4ed8-aea4-16de1cba21c4">IWorkspaceRegistration2</a>
 

 

