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

# IComInstance2Events::OnObjectCreate2


## -description


Generated when a client creates an object.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidActivity [in]

The identifier of the activity in which the object is created.


### -param clsid [in]

The CLSID of the object being created.


### -param tsid [in]

The transaction stream identifier, which is unique for correlation to objects.


### -param CtxtID [in]

The context identifier for this object.


### -param ObjectID [in]

The initial JIT-activated object.


### -param guidPartition [in]

The partition identifier for which this instance is created.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/2fb2904d-7069-4303-bb3c-2caef9499c1e">IComInstance2Events</a>
 

 

