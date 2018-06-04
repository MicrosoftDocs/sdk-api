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

# IInternalUnknown::QueryInternalInterface


## -description


Retrieves pointers to the supported internal interfaces on an object.


## -parameters




### -param riid [in]

The identifier of the internal interface being requested.


### -param ppv [out]

The address of a pointer variable that receives the interface pointer requested in the <i>riid</i> parameter. Upon successful return, *<i>ppv</i> contains the requested interface pointer to the object. If the object does not support the interface, *<i>ppv</i> is set to <b>NULL</b>.


## -returns



This method returns S_OK if the interface is supported, and E_NOINTERFACE otherwise.




## -remarks



This method is similar to the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method, except that the COM proxy manager, when aggregated, will not expose some interfaces through <b>QueryInterface</b>. Instead, those internal interfaces must be exposed through <b>QueryInternalInterface</b>.





## -see-also




<a href="https://msdn.microsoft.com/d2f4c8bc-80b9-4ba0-9f30-f0864144902b">IInternalUnknown</a>



<a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a>
 

 

