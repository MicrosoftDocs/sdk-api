---
UID: NF:workspaceruntime.IWorkspaceScriptable.OnAuthenticated
title: IWorkspaceScriptable::OnAuthenticated (workspaceruntime.h)
description: Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area.
helpviewer_keywords: ["IWorkspaceScriptable interface [Remote Desktop Services]","OnAuthenticated method","IWorkspaceScriptable.OnAuthenticated","IWorkspaceScriptable2 interface [Remote Desktop Services]","OnAuthenticated method","IWorkspaceScriptable2::OnAuthenticated","IWorkspaceScriptable3 interface [Remote Desktop Services]","OnAuthenticated method","IWorkspaceScriptable3::OnAuthenticated","IWorkspaceScriptable::OnAuthenticated","OnAuthenticated","OnAuthenticated method [Remote Desktop Services]","OnAuthenticated method [Remote Desktop Services]","IWorkspaceScriptable interface","OnAuthenticated method [Remote Desktop Services]","IWorkspaceScriptable2 interface","OnAuthenticated method [Remote Desktop Services]","IWorkspaceScriptable3 interface","OnAuthenticated method [Remote Desktop Services]","Workspace object","Workspace object [Remote Desktop Services]","OnAuthenticated method","termserv.iworkspacescriptable_onauthenticated","workspaceruntime/IWorkspaceScriptable2::OnAuthenticated","workspaceruntime/IWorkspaceScriptable3::OnAuthenticated","workspaceruntime/IWorkspaceScriptable::OnAuthenticated"]
old-location: termserv\iworkspacescriptable_onauthenticated.htm
tech.root: TermServ
ms.assetid: 4675fa5b-ea73-4046-a7f9-0b237bd283df
ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable interface [Remote Desktop Services],OnAuthenticated method, IWorkspaceScriptable.OnAuthenticated, IWorkspaceScriptable2 interface [Remote Desktop Services],OnAuthenticated method, IWorkspaceScriptable2::OnAuthenticated, IWorkspaceScriptable3 interface [Remote Desktop Services],OnAuthenticated method, IWorkspaceScriptable3::OnAuthenticated, IWorkspaceScriptable::OnAuthenticated, OnAuthenticated, OnAuthenticated method [Remote Desktop Services], OnAuthenticated method [Remote Desktop Services],IWorkspaceScriptable interface, OnAuthenticated method [Remote Desktop Services],IWorkspaceScriptable2 interface, OnAuthenticated method [Remote Desktop Services],IWorkspaceScriptable3 interface, OnAuthenticated method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],OnAuthenticated method, termserv.iworkspacescriptable_onauthenticated, workspaceruntime/IWorkspaceScriptable2::OnAuthenticated, workspaceruntime/IWorkspaceScriptable3::OnAuthenticated, workspaceruntime/IWorkspaceScriptable::OnAuthenticated
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
 - IWorkspaceScriptable::OnAuthenticated
 - workspaceruntime/IWorkspaceScriptable::OnAuthenticated
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
 - IWorkspaceScriptable.OnAuthenticated
 - IWorkspaceScriptable2.OnAuthenticated
 - IWorkspaceScriptable3.OnAuthenticated
 - Workspace.OnAuthenticated
---

# IWorkspaceScriptable::OnAuthenticated


## -description

Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area. The <b>OnAuthenticated</b> method also resets the credential time-out.

## -parameters

### -param bstrWorkspaceId [in]

A string that contains the connection ID.

### -param bstrUserName [in]

A string that contains a user name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable">IWorkspaceScriptable</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2">IWorkspaceScriptable2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3">IWorkspaceScriptable3</a>