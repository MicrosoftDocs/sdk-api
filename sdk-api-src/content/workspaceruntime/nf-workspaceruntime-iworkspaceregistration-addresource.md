---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWorkspaceRegistration::AddResource


## -description


Adds a resource to the connection in RemoteApp and Desktop Connection.


## -parameters




### -param pUnk [in]

A pointer to the <a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a> object  that called this method.


### -param pdwCookie [out]

A pointer to a <b>DWORD</b> variable to receive the connection cookie for a new resource.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/29e7da7b-7da2-4000-8f3d-d12aa7e12fed">IWorkspaceRegistration</a>



<a href="https://msdn.microsoft.com/b677863a-c8cc-4ed8-aea4-16de1cba21c4">IWorkspaceRegistration2</a>
 

 

