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

# IRpcOptions::Set


## -description


Sets the value of an RPC binding option property.


## -parameters




### -param pPrx [in]

A pointer to the proxy whose property is being set.


### -param dwProperty [in]

An identifier of the property to be set, which must be COMBND_RPCTIMEOUT.


### -param dwValue [in]

The new value of the property.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



See <a href="https://msdn.microsoft.com/aa5db8ac-4c29-43cf-a7ed-a870df9dfb82">IRpcOptions</a> for a table of the possible values of the COMBND_RPCTIMEOUT property.




## -see-also




<a href="https://msdn.microsoft.com/aa5db8ac-4c29-43cf-a7ed-a870df9dfb82">IRpcOptions</a>
 

 

