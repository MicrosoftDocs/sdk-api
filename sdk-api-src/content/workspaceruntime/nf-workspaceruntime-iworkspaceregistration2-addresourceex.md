---
UID: NF:workspaceruntime.IWorkspaceRegistration2.AddResourceEx
title: IWorkspaceRegistration2::AddResourceEx
author: windows-sdk-content
description: Adds a resource to the connection in RemoteApp and Desktop Connection.
old-location: termserv\iworkspaceregistration2_addresourceex.htm
old-project: TermServ
ms.assetid: 7bb26842-ca30-40e2-b7a2-474dda4ad433
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: AddResourceEx, AddResourceEx method [Remote Desktop Services], AddResourceEx method [Remote Desktop Services],IWorkspaceRegistration2 interface, AddResourceEx method [Remote Desktop Services],Workspace object, IWorkspaceRegistration2 interface [Remote Desktop Services],AddResourceEx method, IWorkspaceRegistration2.AddResourceEx, IWorkspaceRegistration2::AddResourceEx, Workspace object [Remote Desktop Services],AddResourceEx method, termserv.iworkspaceregistration2_addresourceex, workspaceruntime/IWorkspaceRegistration2::AddResourceEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
 -
api_name:
 - IWorkspaceRegistration2::AddResourceEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceRegistration2::AddResourceEx


## -description


Not implemented.

Adds a resource to the connection in RemoteApp and Desktop Connection.


## -parameters




### -param pUnk [in]

A pointer to the <a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a> object  that called this method.


### -param bstrEventLogUploadAddress [in]

TBD


### -param pdwCookie [out]

A pointer to a <b>DWORD</b> variable to receive the connection cookie for a new resource.


### -param correlationId [in]

TBD


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b677863a-c8cc-4ed8-aea4-16de1cba21c4">IWorkspaceRegistration2</a>
 

 

