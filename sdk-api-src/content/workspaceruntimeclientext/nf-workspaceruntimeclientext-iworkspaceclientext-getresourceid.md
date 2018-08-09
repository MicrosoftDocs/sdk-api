---
UID: NF:workspaceruntimeclientext.IWorkspaceClientExt.GetResourceId
title: IWorkspaceClientExt::GetResourceId
author: windows-sdk-content
description: Returns the ID of the custom client in RemoteApp and Desktop Connection.
old-location: termserv\iworkspaceclientext_getresourceid.htm
old-project: termserv
ms.assetid: c7a0c77c-0579-48dd-bc06-8ffe48358661
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetResourceId, GetResourceId method [Remote Desktop Services], GetResourceId method [Remote Desktop Services],IWorkspaceClientExt interface, IWorkspaceClientExt interface [Remote Desktop Services],GetResourceId method, IWorkspaceClientExt.GetResourceId, IWorkspaceClientExt::GetResourceId, termserv.iworkspaceclientext_getresourceid, workspaceruntimeclientext/IWorkspaceClientExt::GetResourceId
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Workspaceruntimeclientext.h
api_name:
 - IWorkspaceClientExt.GetResourceId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceClientExt::GetResourceId


## -description


Returns the ID of the custom client in RemoteApp and Desktop Connection.


## -parameters




### -param bstrWorkspaceId [out]

A pointer to a <b>BSTR</b> variable to receive the ID of the custom client. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a>
 

 

