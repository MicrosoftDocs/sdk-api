---
UID: NF:workspaceruntime.IWorkspaceScriptable2.ResourceDismissed
title: IWorkspaceScriptable2::ResourceDismissed (workspaceruntime.h)
description: Alerts the user that a resource has been disabled or otherwise dismissed.
helpviewer_keywords: ["IWorkspaceScriptable2 interface [Remote Desktop Services]","ResourceDismissed method","IWorkspaceScriptable2.ResourceDismissed","IWorkspaceScriptable2::ResourceDismissed","IWorkspaceScriptable3 interface [Remote Desktop Services]","ResourceDismissed method","IWorkspaceScriptable3::ResourceDismissed","ResourceDismissed","ResourceDismissed method [Remote Desktop Services]","ResourceDismissed method [Remote Desktop Services]","IWorkspaceScriptable2 interface","ResourceDismissed method [Remote Desktop Services]","IWorkspaceScriptable3 interface","ResourceDismissed method [Remote Desktop Services]","Workspace object","Workspace object [Remote Desktop Services]","ResourceDismissed method","termserv.iworkspacescriptable2_resourcedismissed","workspaceruntime/IWorkspaceScriptable2::ResourceDismissed","workspaceruntime/IWorkspaceScriptable3::ResourceDismissed"]
old-location: termserv\iworkspacescriptable2_resourcedismissed.htm
tech.root: TermServ
ms.assetid: e45d806c-56de-4f76-a76a-ba6db63f4ac2
ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable2 interface [Remote Desktop Services],ResourceDismissed method, IWorkspaceScriptable2.ResourceDismissed, IWorkspaceScriptable2::ResourceDismissed, IWorkspaceScriptable3 interface [Remote Desktop Services],ResourceDismissed method, IWorkspaceScriptable3::ResourceDismissed, ResourceDismissed, ResourceDismissed method [Remote Desktop Services], ResourceDismissed method [Remote Desktop Services],IWorkspaceScriptable2 interface, ResourceDismissed method [Remote Desktop Services],IWorkspaceScriptable3 interface, ResourceDismissed method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],ResourceDismissed method, termserv.iworkspacescriptable2_resourcedismissed, workspaceruntime/IWorkspaceScriptable2::ResourceDismissed, workspaceruntime/IWorkspaceScriptable3::ResourceDismissed
req.header: workspaceruntime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WorkspaceRuntime.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: WkspRt.exe
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWorkspaceScriptable2::ResourceDismissed
 - workspaceruntime/IWorkspaceScriptable2::ResourceDismissed
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WkspRt.exe
api_name:
 - IWorkspaceScriptable2.ResourceDismissed
 - IWorkspaceScriptable3.ResourceDismissed
 - Workspace.ResourceDismissed
---

# IWorkspaceScriptable2::ResourceDismissed


## -description

Alerts the user that a resource has been disabled or otherwise dismissed.

## -parameters

### -param bstrWorkspaceId [in]

String containing the ID of the workspace that contains the unavailable resource.

### -param bstrWorkspaceFriendlyName [in]

String containing the friendly name of the workspace that holds the unavailable resource.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2">IWorkspaceScriptable2</a>



<a href="/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3">IWorkspaceScriptable3</a>