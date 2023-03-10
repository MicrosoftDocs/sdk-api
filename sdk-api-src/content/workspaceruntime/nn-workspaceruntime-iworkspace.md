---
UID: NN:workspaceruntime.IWorkspace
title: IWorkspace (workspaceruntime.h)
description: Exposes methods that provide information about a connection in RemoteApp and Desktop Connection.
helpviewer_keywords: ["IWorkspace","IWorkspace interface [Remote Desktop Services]","IWorkspace interface [Remote Desktop Services]","described","termserv.iworkspace","workspaceruntime/IWorkspace"]
old-location: termserv\iworkspace.htm
tech.root: TermServ
ms.assetid: 7a94ef42-8a63-4709-816d-1f51a948d486
ms.date: 12/05/2018
ms.keywords: IWorkspace, IWorkspace interface [Remote Desktop Services], IWorkspace interface [Remote Desktop Services],described, termserv.iworkspace, workspaceruntime/IWorkspace
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
 - IWorkspace
 - workspaceruntime/IWorkspace
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
 - IWorkspace
---

# IWorkspace interface


## -description

Exposes methods that provide information about a connection in RemoteApp and Desktop Connection. This interface is implemented by the Remote Desktop Services workspace runtime. These methods are called by custom clients that implement the <a href="/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a> interface.

## -inheritance

The <b>IWorkspace</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWorkspace</b> also has these types of members:

