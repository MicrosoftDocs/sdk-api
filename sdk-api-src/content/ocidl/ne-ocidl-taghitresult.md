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

# tagHITRESULT enumeration


## -description


Indicates whether a location is within the image of an object.


## -enum-fields




### -field HITRESULT_OUTSIDE

The specified location is outside the object and not close to the object.


### -field HITRESULT_TRANSPARENT

The specified location is within the bounds of the object, but not close to the image. For example, a point in the middle of a transparent circle could be HITRESULT_TRANSPARENT.


### -field HITRESULT_CLOSE

The specified location is inside the object or is outside the object but is close enough to the object to be considered inside. Small, thin or detailed objects may use this value. Even if a point is outside the bounding rectangle of an object it may still be close. This value is needed for hitting small objects.


### -field HITRESULT_HIT

The specified location is within the image of the object.


## -see-also




<a href="https://msdn.microsoft.com/a9ee26c4-cf5f-4ca9-b40a-0522097a2f07">IViewObjectEx::QueryHitPoint</a>



<a href="https://msdn.microsoft.com/eb155424-e74c-497f-a9c0-33ed3b2b5513">IViewObjectEx::QueryHitRect</a>
 

 

