---
UID: NF:workspaceruntime.IWorkspaceRegistration.RemoveResource
title: IWorkspaceRegistration::RemoveResource method
author: windows-driver-content
description: Notifies the RemoteApp and Desktop Connection runtime that the client is disconnecting the connection.
old-location: termserv\iworkspaceregistration_removeresource.htm
old-project: TermServ
ms.assetid: f700e3c2-06fe-4f98-9b1e-aeadc339ed7a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IWorkspaceRegistration, IWorkspaceRegistration interface [Remote Desktop Services], RemoveResource method, IWorkspaceRegistration2 interface [Remote Desktop Services], RemoveResource method, IWorkspaceRegistration2::RemoveResource, IWorkspaceRegistration::RemoveResource, RemoveResource method [Remote Desktop Services], RemoveResource method [Remote Desktop Services], IWorkspaceRegistration interface, RemoveResource method [Remote Desktop Services], IWorkspaceRegistration2 interface, RemoveResource method [Remote Desktop Services], Workspace object, RemoveResource,IWorkspaceRegistration.RemoveResource, Workspace object [Remote Desktop Services], RemoveResource method, termserv.iworkspaceregistration_removeresource, workspaceruntime/IWorkspaceRegistration2::RemoveResource, workspaceruntime/IWorkspaceRegistration::RemoveResource
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
-	IWorkspaceRegistration.RemoveResource
-	IWorkspaceRegistration2.RemoveResource
-	Workspace.RemoveResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceRegistration::RemoveResource method


## -description


Notifies the RemoteApp and Desktop Connection runtime that  the client is disconnecting the connection.


## -parameters




### -param dwCookieConnection [in]

A <b>DWORD</b> value that contains a connection cookie returned by the <a href="https://msdn.microsoft.com/cd4ed8a0-e5a8-4809-a9bd-d013a84b0bd4">AddResource</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/29e7da7b-7da2-4000-8f3d-d12aa7e12fed">IWorkspaceRegistration</a>



<a href="https://msdn.microsoft.com/b677863a-c8cc-4ed8-aea4-16de1cba21c4">IWorkspaceRegistration2</a>
 

 

