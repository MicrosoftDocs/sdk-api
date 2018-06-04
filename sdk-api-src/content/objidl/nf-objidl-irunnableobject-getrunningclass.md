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

# IRunnableObject::GetRunningClass


## -description


Retrieves the CLSID of a running object.


## -parameters




### -param lpClsid [out]

A pointer to the object's class identifier.


## -returns



This method can return the standard return values E_INVALIDARG, E_UNEXPECTED, and S_OK.




## -remarks



If an embedded document was created by an application that is not available on the user's computer, the document, by a call to <a href="https://msdn.microsoft.com/d871879f-ec68-48e1-8ef6-364cf1447d0f">CoTreatAsClass</a>, may be able to display itself for editing by emulating a class that is supported on the user's machine. In this case, the CLSID returned by a call to <b>IRunnableObject::GetRunningClass</b> will be that of the class being emulated, rather than the document's native class.




## -see-also




<a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>
 

 

