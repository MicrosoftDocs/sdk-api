---
UID: NN:workspaceruntime.IWorkspaceRegistration
title: IWorkspaceRegistration (workspaceruntime.h)
description: Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection. (IWorkspaceRegistration)
helpviewer_keywords: ["IWorkspaceRegistration","IWorkspaceRegistration interface [Remote Desktop Services]","IWorkspaceRegistration interface [Remote Desktop Services]","described","termserv.iworkspaceregistration","workspaceruntime/IWorkspaceRegistration"]
old-location: termserv\iworkspaceregistration.htm
tech.root: TermServ
ms.assetid: 29e7da7b-7da2-4000-8f3d-d12aa7e12fed
ms.date: 12/05/2018
ms.keywords: IWorkspaceRegistration, IWorkspaceRegistration interface [Remote Desktop Services], IWorkspaceRegistration interface [Remote Desktop Services],described, termserv.iworkspaceregistration, workspaceruntime/IWorkspaceRegistration
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
 - IWorkspaceRegistration
 - workspaceruntime/IWorkspaceRegistration
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
 - IWorkspaceRegistration
---

# IWorkspaceRegistration interface


## -description

Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection. These methods are called by custom clients that implement the <a href="/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a> interface.

## -inheritance

The <b>IWorkspaceRegistration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWorkspaceRegistration</b> also has these types of members:

