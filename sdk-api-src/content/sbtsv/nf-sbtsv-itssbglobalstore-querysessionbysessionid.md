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

# ITsSbGlobalStore::QuerySessionBySessionId


## -description


Retrieves the <a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a> object associated with the given 
session ID.


## -parameters




### -param ProviderName [in]

The resource plug-in provider name that owns the target.


### -param dwSessionId [in]

The session ID.


### -param TargetName [in]

The name of the target computer on which this session is present.


### -param ppSession [out]

A pointer to a pointer to a session object. When you have finished using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


## -returns



This method can return one of these values.




## -remarks



Any changes made to the target objects returned by this method do not affect the target objects stored 
in Remote Desktop Connection Broker (RD Connection Broker). The target objects returned are copies of the target objects in RD Connection Broker.




## -see-also




<a href="https://msdn.microsoft.com/d25b6f73-ee5f-40e4-9c49-fd48dd3990d2">ITsSbGlobalStore</a>
 

 

