---
UID: NN:workspaceax.IWorkspaceResTypeRegistry
title: IWorkspaceResTypeRegistry (workspaceax.h)
description: Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime.
helpviewer_keywords: ["IWorkspaceResTypeRegistry","IWorkspaceResTypeRegistry interface [Remote Desktop Services]","IWorkspaceResTypeRegistry interface [Remote Desktop Services]","described","termserv.iworkspacerestyperegistry","workspaceax/IWorkspaceResTypeRegistry"]
old-location: termserv\iworkspacerestyperegistry.htm
tech.root: TermServ
ms.assetid: bea617a0-cd64-4c77-af27-b418178e3dad
ms.date: 12/05/2018
ms.keywords: IWorkspaceResTypeRegistry, IWorkspaceResTypeRegistry interface [Remote Desktop Services], IWorkspaceResTypeRegistry interface [Remote Desktop Services],described, termserv.iworkspacerestyperegistry, workspaceax/IWorkspaceResTypeRegistry
req.header: workspaceax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Tsworkspace.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWorkspaceResTypeRegistry
 - workspaceax/IWorkspaceResTypeRegistry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tsworkspace.dll
api_name:
 - IWorkspaceResTypeRegistry
---

# IWorkspaceResTypeRegistry interface


## -description

Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime. This interface is implemented by the Remote Desktop Services workspace runtime. These methods are called by custom clients.

## -inheritance

The <b>IWorkspaceResTypeRegistry</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWorkspaceResTypeRegistry</b> also has these types of members:

