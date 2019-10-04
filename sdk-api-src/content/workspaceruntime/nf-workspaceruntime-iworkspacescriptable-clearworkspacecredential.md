---
UID: NF:workspaceruntime.IWorkspaceScriptable.ClearWorkspaceCredential
title: IWorkspaceScriptable::ClearWorkspaceCredential (workspaceruntime.h)
author: windows-sdk-content
description: Deletes the user credentials associated with the specified connection ID.
old-location: termserv\iworkspacescriptable_clearworkspacecredential.htm
tech.root: TermServ
ms.assetid: f21df395-3ff7-43c0-b1cd-010ae2c1d16b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClearWorkspaceCredential, ClearWorkspaceCredential method [Remote Desktop Services], ClearWorkspaceCredential method [Remote Desktop Services],IWorkspaceScriptable interface, ClearWorkspaceCredential method [Remote Desktop Services],IWorkspaceScriptable2 interface, ClearWorkspaceCredential method [Remote Desktop Services],IWorkspaceScriptable3 interface, ClearWorkspaceCredential method [Remote Desktop Services],Workspace object, IWorkspaceScriptable interface [Remote Desktop Services],ClearWorkspaceCredential method, IWorkspaceScriptable.ClearWorkspaceCredential, IWorkspaceScriptable2 interface [Remote Desktop Services],ClearWorkspaceCredential method, IWorkspaceScriptable2::ClearWorkspaceCredential, IWorkspaceScriptable3 interface [Remote Desktop Services],ClearWorkspaceCredential method, IWorkspaceScriptable3::ClearWorkspaceCredential, IWorkspaceScriptable::ClearWorkspaceCredential, Workspace object [Remote Desktop Services],ClearWorkspaceCredential method, termserv.iworkspacescriptable_clearworkspacecredential, workspaceruntime/IWorkspaceScriptable2::ClearWorkspaceCredential, workspaceruntime/IWorkspaceScriptable3::ClearWorkspaceCredential, workspaceruntime/IWorkspaceScriptable::ClearWorkspaceCredential
ms.topic: method
f1_keywords: 
 - "workspaceruntime/IWorkspaceScriptable.ClearWorkspaceCredential"
dev_langs:
 - c++
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
 - IWorkspaceScriptable.ClearWorkspaceCredential
 - IWorkspaceScriptable2.ClearWorkspaceCredential
 - IWorkspaceScriptable3.ClearWorkspaceCredential
 - Workspace.ClearWorkspaceCredential
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable">IWorkspaceScriptable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2">IWorkspaceScriptable2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3">IWorkspaceScriptable3</a>
 

 

