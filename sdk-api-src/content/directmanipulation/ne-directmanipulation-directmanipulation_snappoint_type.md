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

# DIRECTMANIPULATION_SNAPPOINT_TYPE enumeration


## -description


Modifies how the final inertia end position is calculated.


## -enum-fields




### -field DIRECTMANIPULATION_SNAPPOINT_MANDATORY

Content always stops at the snap point closest to where inertia would naturally stop along the direction of inertia.


### -field DIRECTMANIPULATION_SNAPPOINT_OPTIONAL

Content stops at a snap point closest to where inertia would naturally stop along the direction of inertia, depending on how close the snap point is. 


### -field DIRECTMANIPULATION_SNAPPOINT_MANDATORY_SINGLE

Content always stops at the snap point closest to the release point along the direction of inertia.


### -field DIRECTMANIPULATION_SNAPPOINT_OPTIONAL_SINGLE

Content stops at the next snap point, if the motion starts far from it.


## -remarks



For <b>DIRECTMANIPULATION_SNAPPOINT_MANDATORY</b> or <b>DIRECTMANIPULATION_SNAPPOINT_OPTIONAL</b> snap points, the snap points are chosen based on the natural ending position of inertia as calculated by the touch interaction engine. For <b>DIRECTMANIPULATION_SNAPPOINT_MANDATORY_SINGLE</b> or <b>DIRECTMANIPULATION_SNAPPOINT_OPTIONAL_SINGLE</b> snap points, the selected snap point depends on where inertia started.




## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>
 

 

