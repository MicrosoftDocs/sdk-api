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

# DIRECTMANIPULATION_SNAPPOINT_COORDINATE enumeration


## -description


Defines the coordinate system for a collection of snap points.


## -enum-fields




### -field DIRECTMANIPULATION_COORDINATE_BOUNDARY

Default. 

Snap points are specified relative to the top and left boundaries of the content unless <b>DIRECTMANIPULATION_COORDINATE_MIRRORED</b> is also specified, in which case they are relative to the bottom and right boundaries of the content. For zoom, the boundary is 1.0f.


### -field DIRECTMANIPULATION_COORDINATE_ORIGIN

Snap points are specified relative to the origin of the viewport.


### -field DIRECTMANIPULATION_COORDINATE_MIRRORED

Snap points are interpreted as specified in the negative direction of the origin. The origin is shifted to the bottom and right of the viewport or content. Cannot be set for zoom.


## -remarks



If <b>DIRECTMANIPULATION_COORDINATE_ORIGIN</b> and <b>DIRECTMANIPULATION_COORDINATE_MIRRORED</b> are both specified, the snap points are interpreted as specified from the bottom and right boundaries of the content (the size of the content - the size of the viewport). This is intended for RTL reading scenarios where content is normally specified and rendered from right-to-left or bottom-to-top.




## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>



<a href="https://msdn.microsoft.com/3f9afe1b-20f4-45fa-a63b-25b7a0c597af">SetSnapCoordinate</a>
 

 

