---
UID: NF:workspaceruntime.IWorkspaceScriptable.IsWorkspaceCredentialSpecified
title: IWorkspaceScriptable::IsWorkspaceCredentialSpecified (workspaceruntime.h)
author: windows-sdk-content
description: Determines whether user credentials exist for the specified connection ID.
old-location: termserv\iworkspacescriptable_isworkspacecredentialspecified.htm
tech.root: TermServ
ms.assetid: 1b01f48d-161a-4cea-84d4-82c98d2e6998
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable interface [Remote Desktop Services],IsWorkspaceCredentialSpecified method, IWorkspaceScriptable.IsWorkspaceCredentialSpecified, IWorkspaceScriptable2 interface [Remote Desktop Services],IsWorkspaceCredentialSpecified method, IWorkspaceScriptable2::IsWorkspaceCredentialSpecified, IWorkspaceScriptable3 interface [Remote Desktop Services],IsWorkspaceCredentialSpecified method, IWorkspaceScriptable3::IsWorkspaceCredentialSpecified, IWorkspaceScriptable::IsWorkspaceCredentialSpecified, IsWorkspaceCredentialSpecified, IsWorkspaceCredentialSpecified method [Remote Desktop Services], IsWorkspaceCredentialSpecified method [Remote Desktop Services],IWorkspaceScriptable interface, IsWorkspaceCredentialSpecified method [Remote Desktop Services],IWorkspaceScriptable2 interface, IsWorkspaceCredentialSpecified method [Remote Desktop Services],IWorkspaceScriptable3 interface, IsWorkspaceCredentialSpecified method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],IsWorkspaceCredentialSpecified method, termserv.iworkspacescriptable_isworkspacecredentialspecified, workspaceruntime/IWorkspaceScriptable2::IsWorkspaceCredentialSpecified, workspaceruntime/IWorkspaceScriptable3::IsWorkspaceCredentialSpecified, workspaceruntime/IWorkspaceScriptable::IsWorkspaceCredentialSpecified
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
 - IWorkspaceScriptable.IsWorkspaceCredentialSpecified
 - IWorkspaceScriptable2.IsWorkspaceCredentialSpecified
 - IWorkspaceScriptable3.IsWorkspaceCredentialSpecified
 - Workspace.IsWorkspaceCredentialSpecified
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspaceScriptable::IsWorkspaceCredentialSpecified


## -description


Determines whether user credentials exist for the specified connection ID.


## -parameters




### -param bstrWorkspaceId [in]

A string that contains the connection ID.


### -param bCountUnauthenticatedCredentials [in]

<b>VARIANT_TRUE</b> to specify that the <i>pbCredExist</i> parameter should return <b>VARIANT_TRUE</b> if credentials (authenticated or unauthenticated) exist for the connection ID specified in the <i>bstrWorkspaceId</i> parameter. <b>VARIANT_FALSE</b> to specify that the <i>pbCredExist</i> parameter should return <b>VARIANT_TRUE</b> only if authenticated credentials exist for the connection ID specified in the <i>bstrWorkspaceId</i> parameter.


### -param pbCredExist [out, retval]

A pointer to a <b>VARIANT_BOOL</b> variable to receive whether credentials exist for the connection ID specified in the <i>bstrWorkspaceId</i> parameter. This value is <b>VARIANT_TRUE</b> if credentials exist; otherwise, <b>VARIANT_FALSE</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b6591369-d73f-4c7d-8525-428dffc9a341">IWorkspaceScriptable</a>



<a href="https://msdn.microsoft.com/66a6c283-bef9-4cb4-9035-d4a2d2cb7b4f">IWorkspaceScriptable2</a>



<a href="https://msdn.microsoft.com/6fe02f0a-8cce-47f0-807e-e627336adf2c">IWorkspaceScriptable3</a>
 

 

