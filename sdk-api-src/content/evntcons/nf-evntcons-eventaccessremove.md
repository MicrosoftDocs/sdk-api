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

# EventAccessRemove function


## -description


Removes the permissions defined in the registry for the specified provider or session.


## -parameters




### -param Guid [in]

GUID that uniquely identifies the provider or session whose permissions you want to remove from the 
      registry.


## -returns



Returns ERROR_SUCCESS if successful.




## -remarks



After removing the permission from the registry, the default permissions apply to the provider or session. For 
    details on the default permissions, see 
    <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>.




## -see-also




<a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>



<a href="https://msdn.microsoft.com/21c87137-0e8f-43d1-9dad-9f2b4fc591a3">EventAccessQuery</a>
 

 

