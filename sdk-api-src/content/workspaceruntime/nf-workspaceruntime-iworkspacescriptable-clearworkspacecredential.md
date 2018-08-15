---
UID: NF:workspaceruntime.IWorkspaceScriptable.ClearWorkspaceCredential
title: IWorkspaceScriptable::ClearWorkspaceCredential
author: windows-sdk-content
description: Deletes the user credentials associated with the specified connection ID.
old-location: termserv\iworkspacescriptable_clearworkspacecredential.htm
old-project: termserv
ms.assetid: f21df395-3ff7-43c0-b1cd-010ae2c1d16b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClearWorkspaceCredential, ClearWorkspaceCredential method [Remote Desktop Services], ClearWorkspaceCredential method [Remote Desktop Services],IWorkspaceScriptable interface, ClearWorkspaceCredential method [Remote Desktop Services],IWorkspaceScriptable2 interface, ClearWorkspaceCredential method [Remote Desktop Services],IWorkspaceScriptable3 interface, ClearWorkspaceCredential method [Remote Desktop Services],Workspace object, IWorkspaceScriptable interface [Remote Desktop Services],ClearWorkspaceCredential method, IWorkspaceScriptable.ClearWorkspaceCredential, IWorkspaceScriptable2 interface [Remote Desktop Services],ClearWorkspaceCredential method, IWorkspaceScriptable2::ClearWorkspaceCredential, IWorkspaceScriptable3 interface [Remote Desktop Services],ClearWorkspaceCredential method, IWorkspaceScriptable3::ClearWorkspaceCredential, IWorkspaceScriptable::ClearWorkspaceCredential, Workspace object [Remote Desktop Services],ClearWorkspaceCredential method, termserv.iworkspacescriptable_clearworkspacecredential, workspaceruntime/IWorkspaceScriptable2::ClearWorkspaceCredential, workspaceruntime/IWorkspaceScriptable3::ClearWorkspaceCredential, workspaceruntime/IWorkspaceScriptable::ClearWorkspaceCredential
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: workspaceruntime.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wksprt.exe
api_name:
 - IWorkspaceScriptable.ClearWorkspaceCredential
 - IWorkspaceScriptable2.ClearWorkspaceCredential
 - IWorkspaceScriptable3.ClearWorkspaceCredential
 - Workspace.ClearWorkspaceCredential
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceScriptable::ClearWorkspaceCredential


## -description


Deletes the user credentials associated with the specified connection ID.


## -parameters




### -param bstrWorkspaceId [in]

A string that contains a connection ID.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the connection ID has no active connections, it is removed from the credential store.




## -see-also




<a href="https://msdn.microsoft.com/b6591369-d73f-4c7d-8525-428dffc9a341">IWorkspaceScriptable</a>



<a href="https://msdn.microsoft.com/66a6c283-bef9-4cb4-9035-d4a2d2cb7b4f">IWorkspaceScriptable2</a>



<a href="https://msdn.microsoft.com/6fe02f0a-8cce-47f0-807e-e627336adf2c">IWorkspaceScriptable3</a>
 

 

