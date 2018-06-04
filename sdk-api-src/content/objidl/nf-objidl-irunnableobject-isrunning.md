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

# IRunnableObject::IsRunning


## -description


Determines whether an object is currently in the running state.


## -parameters






## -returns



If the object is in the running state, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.




## -remarks



A container application could call <b>IRunnableObject::IsRunning</b> when it needs to know if the server is immediately available. For example, a container's implementation of the <a href="https://msdn.microsoft.com/08569037-7ecd-4e63-9f94-c2552c327800">IOleItemContainer::GetObject</a> method would return an error if the server is not running and the bindspeed parameter specifies BINDSPEED_IMMEDIATE.

An object handler could call <b>IRunnableObject::IsRunning</b> when it wants to avoid conflicts with a running server or when the running server might have more up-to-date information. For example, a handler's implementation of <a href="https://msdn.microsoft.com/babaf55e-6c43-48d8-ad13-1333e29a3e1d">IOleObject::GetExtent</a> would delegate to the object server if it is running, because the server's information might be more current than that in the handler's cache.


<a href="https://msdn.microsoft.com/9392666f-c269-4667-aeac-67c68bcc5f06">OleIsRunning</a> is a helper function that conveniently repackages the functionality offered by <b>IRunnableObject::IsRunning</b>. With the release of OLE 2.01, the implementation of <b>OleIsRunning</b> was changed so that it calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a>, asks for <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>, and then calls <b>IRunnableObject::IsRunning</b>. In other words, you can use the interface and the helper function interchangeably.




## -see-also




<a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>



<a href="https://msdn.microsoft.com/9392666f-c269-4667-aeac-67c68bcc5f06">OleIsRunning</a>
 

 

