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

# OleIsRunning function


## -description


Determines whether a compound document object is currently in the running state.




## -parameters




### -param pObject [in]

Pointer to the <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> interface on the object of interest.


## -returns



The return value is <b>TRUE</b> if the object is running; otherwise, it is <b>FALSE</b>.





## -remarks



You can use <b>OleIsRunning</b> and <a href="https://msdn.microsoft.com/0a4cdd21-8256-4533-9cad-d9e8450a17e9">IRunnableObject::IsRunning</a> interchangeably. <b>OleIsRunning</b> queries the object for a pointer to the <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a> interface and calls its <b>IRunnableObject::IsRunning</b> method. If successful, the function returns the results of the call to <b>IRunnableObject::IsRunning</b>.






## -see-also




<a href="https://msdn.microsoft.com/0a4cdd21-8256-4533-9cad-d9e8450a17e9">IRunnableObject::IsRunning</a>
 

 

