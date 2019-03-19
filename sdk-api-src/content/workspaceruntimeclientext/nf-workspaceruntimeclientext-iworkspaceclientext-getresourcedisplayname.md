---
UID: NF:workspaceruntimeclientext.IWorkspaceClientExt.GetResourceDisplayName
title: IWorkspaceClientExt::GetResourceDisplayName (workspaceruntimeclientext.h)
author: windows-sdk-content
description: Returns the display name of the custom client in RemoteApp and Desktop Connection.
old-location: termserv\iworkspaceclientext_getresourcedisplayname.htm
tech.root: TermServ
ms.assetid: f67fa6f3-621a-4015-8fcf-85b1302a3c8a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetResourceDisplayName, GetResourceDisplayName method [Remote Desktop Services], GetResourceDisplayName method [Remote Desktop Services],IWorkspaceClientExt interface, IWorkspaceClientExt interface [Remote Desktop Services],GetResourceDisplayName method, IWorkspaceClientExt.GetResourceDisplayName, IWorkspaceClientExt::GetResourceDisplayName, termserv.iworkspaceclientext_getresourcedisplayname, workspaceruntimeclientext/IWorkspaceClientExt::GetResourceDisplayName
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Workspaceruntimeclientext.h
api_name:
 - IWorkspaceClientExt.GetResourceDisplayName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspaceClientExt::GetResourceDisplayName


## -description


Returns the display name of the custom client in RemoteApp and Desktop Connection.


## -parameters




### -param bstrWorkspaceDisplayName [out]

A pointer to a <b>BSTR</b> variable to receive the display name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a>
 

 

