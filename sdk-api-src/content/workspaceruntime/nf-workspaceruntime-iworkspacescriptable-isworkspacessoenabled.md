---
UID: NF:workspaceruntime.IWorkspaceScriptable.IsWorkspaceSSOEnabled
title: IWorkspaceScriptable::IsWorkspaceSSOEnabled (workspaceruntime.h)
author: windows-sdk-content
description: Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.
old-location: termserv\iworkspacescriptable_isworkspacessoenabled.htm
tech.root: TermServ
ms.assetid: 54608723-9a17-4bf2-a46d-8fed52378767
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable interface [Remote Desktop Services],IsWorkspaceSSOEnabled method, IWorkspaceScriptable.IsWorkspaceSSOEnabled, IWorkspaceScriptable2 interface [Remote Desktop Services],IsWorkspaceSSOEnabled method, IWorkspaceScriptable2::IsWorkspaceSSOEnabled, IWorkspaceScriptable3 interface [Remote Desktop Services],IsWorkspaceSSOEnabled method, IWorkspaceScriptable3::IsWorkspaceSSOEnabled, IWorkspaceScriptable::IsWorkspaceSSOEnabled, IsWorkspaceSSOEnabled, IsWorkspaceSSOEnabled method [Remote Desktop Services], IsWorkspaceSSOEnabled method [Remote Desktop Services],IWorkspaceScriptable interface, IsWorkspaceSSOEnabled method [Remote Desktop Services],IWorkspaceScriptable2 interface, IsWorkspaceSSOEnabled method [Remote Desktop Services],IWorkspaceScriptable3 interface, IsWorkspaceSSOEnabled method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],IsWorkspaceSSOEnabled method, termserv.iworkspacescriptable_isworkspacessoenabled, workspaceruntime/IWorkspaceScriptable2::IsWorkspaceSSOEnabled, workspaceruntime/IWorkspaceScriptable3::IsWorkspaceSSOEnabled, workspaceruntime/IWorkspaceScriptable::IsWorkspaceSSOEnabled
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
 - IWorkspaceScriptable.IsWorkspaceSSOEnabled
 - IWorkspaceScriptable2.IsWorkspaceSSOEnabled
 - IWorkspaceScriptable3.IsWorkspaceSSOEnabled
 - Workspace.IsWorkspaceSSOEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWorkspaceScriptable::IsWorkspaceSSOEnabled


## -description


Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.


## -parameters




### -param pbSSOEnabled [out, retval]

A pointer to a <b>VARIANT_BOOL</b> variable to receive  whether SSO is enabled. This value is <b>VARIANT_TRUE</b> if SSO is enabled; otherwise, <b>VARIANT_FALSE</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b6591369-d73f-4c7d-8525-428dffc9a341">IWorkspaceScriptable</a>



<a href="https://msdn.microsoft.com/66a6c283-bef9-4cb4-9035-d4a2d2cb7b4f">IWorkspaceScriptable2</a>



<a href="https://msdn.microsoft.com/6fe02f0a-8cce-47f0-807e-e627336adf2c">IWorkspaceScriptable3</a>
 

 

