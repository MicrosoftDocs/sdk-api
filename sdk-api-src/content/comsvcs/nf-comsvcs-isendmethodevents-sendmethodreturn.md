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

# ISendMethodEvents::SendMethodReturn


## -description


Generated when a method called through a component interface returns control to the caller.


## -parameters




### -param pIdentity [in]

A pointer to the interface used to call the method.


### -param riid [in]

The ID of the interface used to call the method.


### -param dwMeth [in]

The method called.


### -param hrCall [in]

The result returned by the method call.


### -param hrServer [in]

The result returned by the DCOM call to the server on which the component lives.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/d1437581-8a2b-4e88-aa12-a16eb9f40125">ISendMethodEvents</a>
 

 

