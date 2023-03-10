---
UID: NF:workspaceruntimeclientext.IWorkspaceClientExt.GetResourceDisplayName
title: IWorkspaceClientExt::GetResourceDisplayName (workspaceruntimeclientext.h)
description: Returns the display name of the custom client in RemoteApp and Desktop Connection.
helpviewer_keywords: ["GetResourceDisplayName","GetResourceDisplayName method [Remote Desktop Services]","GetResourceDisplayName method [Remote Desktop Services]","IWorkspaceClientExt interface","IWorkspaceClientExt interface [Remote Desktop Services]","GetResourceDisplayName method","IWorkspaceClientExt.GetResourceDisplayName","IWorkspaceClientExt::GetResourceDisplayName","termserv.iworkspaceclientext_getresourcedisplayname","workspaceruntimeclientext/IWorkspaceClientExt::GetResourceDisplayName"]
old-location: termserv\iworkspaceclientext_getresourcedisplayname.htm
tech.root: TermServ
ms.assetid: f67fa6f3-621a-4015-8fcf-85b1302a3c8a
ms.date: 12/05/2018
ms.keywords: GetResourceDisplayName, GetResourceDisplayName method [Remote Desktop Services], GetResourceDisplayName method [Remote Desktop Services],IWorkspaceClientExt interface, IWorkspaceClientExt interface [Remote Desktop Services],GetResourceDisplayName method, IWorkspaceClientExt.GetResourceDisplayName, IWorkspaceClientExt::GetResourceDisplayName, termserv.iworkspaceclientext_getresourcedisplayname, workspaceruntimeclientext/IWorkspaceClientExt::GetResourceDisplayName
req.header: workspaceruntimeclientext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Workspaceruntimeclientext.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWorkspaceClientExt::GetResourceDisplayName
 - workspaceruntimeclientext/IWorkspaceClientExt::GetResourceDisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Workspaceruntimeclientext.h
api_name:
 - IWorkspaceClientExt.GetResourceDisplayName
---

# IWorkspaceClientExt::GetResourceDisplayName


## -description

Returns the display name of the custom client in RemoteApp and Desktop Connection.

## -parameters

### -param bstrWorkspaceDisplayName [out]

A pointer to a <b>BSTR</b> variable to receive the display name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a>