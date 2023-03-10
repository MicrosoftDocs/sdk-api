---
UID: NF:workspaceruntimeclientext.IWorkspaceClientExt.GetResourceId
title: IWorkspaceClientExt::GetResourceId (workspaceruntimeclientext.h)
description: Returns the ID of the custom client in RemoteApp and Desktop Connection.
helpviewer_keywords: ["GetResourceId","GetResourceId method [Remote Desktop Services]","GetResourceId method [Remote Desktop Services]","IWorkspaceClientExt interface","IWorkspaceClientExt interface [Remote Desktop Services]","GetResourceId method","IWorkspaceClientExt.GetResourceId","IWorkspaceClientExt::GetResourceId","termserv.iworkspaceclientext_getresourceid","workspaceruntimeclientext/IWorkspaceClientExt::GetResourceId"]
old-location: termserv\iworkspaceclientext_getresourceid.htm
tech.root: TermServ
ms.assetid: c7a0c77c-0579-48dd-bc06-8ffe48358661
ms.date: 12/05/2018
ms.keywords: GetResourceId, GetResourceId method [Remote Desktop Services], GetResourceId method [Remote Desktop Services],IWorkspaceClientExt interface, IWorkspaceClientExt interface [Remote Desktop Services],GetResourceId method, IWorkspaceClientExt.GetResourceId, IWorkspaceClientExt::GetResourceId, termserv.iworkspaceclientext_getresourceid, workspaceruntimeclientext/IWorkspaceClientExt::GetResourceId
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
 - IWorkspaceClientExt::GetResourceId
 - workspaceruntimeclientext/IWorkspaceClientExt::GetResourceId
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
 - IWorkspaceClientExt.GetResourceId
---

# IWorkspaceClientExt::GetResourceId


## -description

Returns the ID of the custom client in RemoteApp and Desktop Connection.

## -parameters

### -param bstrWorkspaceId [out]

A pointer to a <b>BSTR</b> variable to receive the ID of the custom client.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a>