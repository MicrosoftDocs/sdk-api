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

# tagMULTI_QI structure


## -description


Represents an interface in a query for multiple interfaces.


## -struct-fields




### -field pIID

A pointer to an interface identifier.


### -field pItf

A pointer to the interface requested in <b>pIID</b>. This member must be <b>NULL</b> on input.


### -field hr

The return value of the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> call to locate the requested interface. Common return values include S_OK and E_NOINTERFACE. This member must be 0 on input.


## -remarks



To optimize network performance, most remote activation functions take an array of <b>MULTI_QI</b> structures rather than just a single IID as input and a single pointer to the requested interface on the object as output, as do local activation functions. This allows a set of pointers to interfaces to be returned from the same object in a single round-trip to the server. In network scenarios, requesting multiple interfaces at the time of object construction can save considerable time over using a number of calls to <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for unique interfaces, each of which would require a round-trip to the server.

 




## -see-also




<a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a>



<a href="https://msdn.microsoft.com/f8a22f5f-a21f-49e7-bd6c-ca987206ee46">CoGetInstanceFromFile</a>



<a href="https://msdn.microsoft.com/6a77770c-b7e1-4d29-9c4b-331b5950a635">CoGetInstanceFromIStorage</a>



<a href="https://msdn.microsoft.com/5e50396f-2931-403f-946a-dc096cb012cc">IMultiQI</a>
 

 

