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

# IAppDomainHelper::DoCallback


## -description


Switches into a given application domain (which the calling object must be bound to), executes the supplied callback function in that application domain, and then returns to the original application domain.


## -parameters




### -param pUnkAD [in]

Reference to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the application domain that you want to switch to. The object calling <b>DoCallback</b> must be bound to that application domain.


### -param __MIDL__IAppDomainHelper0001




### -param pPool [in]

This parameter is used to provide any data that the callback function might need.


#### - pfnCallbackCB [in]

Reference to the callback function. This function is executed in the application domain that you switched to. The parameter of this function, <i>pv</i>, comes from the <i>pPool</i> parameter, which is defined next.



#### pv


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/2709f284-ca8c-404e-b568-b655f780549a">IAppDomainHelper</a>
 

 

