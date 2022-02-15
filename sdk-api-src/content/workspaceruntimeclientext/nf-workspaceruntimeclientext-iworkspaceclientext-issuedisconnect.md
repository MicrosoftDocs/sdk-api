---
UID: NF:workspaceruntimeclientext.IWorkspaceClientExt.IssueDisconnect
title: IWorkspaceClientExt::IssueDisconnect (workspaceruntimeclientext.h)
description: Disconnects the custom client in RemoteApp and Desktop Connection.
helpviewer_keywords: ["IWorkspaceClientExt interface [Remote Desktop Services]","IssueDisconnect method","IWorkspaceClientExt.IssueDisconnect","IWorkspaceClientExt::IssueDisconnect","IssueDisconnect","IssueDisconnect method [Remote Desktop Services]","IssueDisconnect method [Remote Desktop Services]","IWorkspaceClientExt interface","termserv.iworkspaceclientext_issuedisconnect","workspaceruntimeclientext/IWorkspaceClientExt::IssueDisconnect"]
old-location: termserv\iworkspaceclientext_issuedisconnect.htm
tech.root: TermServ
ms.assetid: 07c2546b-e9bf-46e6-a1de-6da31fa1579b
ms.date: 12/05/2018
ms.keywords: IWorkspaceClientExt interface [Remote Desktop Services],IssueDisconnect method, IWorkspaceClientExt.IssueDisconnect, IWorkspaceClientExt::IssueDisconnect, IssueDisconnect, IssueDisconnect method [Remote Desktop Services], IssueDisconnect method [Remote Desktop Services],IWorkspaceClientExt interface, termserv.iworkspaceclientext_issuedisconnect, workspaceruntimeclientext/IWorkspaceClientExt::IssueDisconnect
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
 - IWorkspaceClientExt::IssueDisconnect
 - workspaceruntimeclientext/IWorkspaceClientExt::IssueDisconnect
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
 - IWorkspaceClientExt.IssueDisconnect
---

# IWorkspaceClientExt::IssueDisconnect


## -description

Disconnects the custom client in RemoteApp and Desktop Connection. The RemoteApp and Desktop Connection runtime calls this method to disconnect the client.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext">IWorkspaceClientExt</a>
