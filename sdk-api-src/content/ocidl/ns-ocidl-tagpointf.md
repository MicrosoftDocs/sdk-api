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

# tagPOINTF structure


## -description


Contains information that is used to convert between container units, expressed in floating point, and control units, expressed in <b>HIMETRIC</b>. The <b>POINTF</b> structure specifically holds the floating point container units. Controls do not attempt to interpret either value in the structure.




## -struct-fields




### -field x

The x coordinates of the point in units that the container finds convenient.


### -field y

The y coordinates of the point in units that the container finds convenient.



## -see-also




<a href="https://msdn.microsoft.com/c7add062-4b42-43be-a982-c881c947f8f0">IOleControlSite::TransformCoords</a>
 

 

