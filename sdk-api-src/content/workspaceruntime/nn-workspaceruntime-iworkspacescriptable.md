---
UID: NN:workspaceruntime.IWorkspaceScriptable
title: IWorkspaceScriptable (workspaceruntime.h)
description: Exposes methods that manage RemoteApp and Desktop Connection credentials and connections. (IWorkspaceScriptable)
helpviewer_keywords: ["IWorkspaceScriptable","IWorkspaceScriptable interface [Remote Desktop Services]","IWorkspaceScriptable interface [Remote Desktop Services]","described","termserv.iworkspacescriptable","workspaceruntime/IWorkspaceScriptable"]
old-location: termserv\iworkspacescriptable.htm
tech.root: TermServ
ms.assetid: b6591369-d73f-4c7d-8525-428dffc9a341
ms.date: 12/05/2018
ms.keywords: IWorkspaceScriptable, IWorkspaceScriptable interface [Remote Desktop Services], IWorkspaceScriptable interface [Remote Desktop Services],described, termserv.iworkspacescriptable, workspaceruntime/IWorkspaceScriptable
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
 - IWorkspaceScriptable
 - workspaceruntime/IWorkspaceScriptable
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
 - IWorkspaceScriptable
---

# IWorkspaceScriptable interface


## -description

Exposes methods that manage RemoteApp and Desktop Connection credentials and connections. This interface is implemented by the RemoteApp and Desktop Connection runtime. These methods are called by custom clients that implement the <a href="/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a> interface.

## -inheritance

The <b>IWorkspaceScriptable</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWorkspaceScriptable</b> also has these types of members:

