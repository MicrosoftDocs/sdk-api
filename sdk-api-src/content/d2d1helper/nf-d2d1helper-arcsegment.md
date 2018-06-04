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

# ArcSegment function


## -description


Creates a <a href="https://msdn.microsoft.com/3f391265-20b4-4897-aa0b-d14b71cd5f0a">D2D1_ARC_SEGMENT</a> structure.


## -parameters




### -param point [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The end point of the arc.




### -param size [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/c2fd41fb-72b3-418b-ad87-65549b04657d">D2D1_SIZE_F</a></b>

The x-radius and y-radius of the arc.




### -param rotationAngle [in]

Type: <b>FLOAT</b>

The number of degrees that the ellipse is rotated relative to the current coordinate system. A positive number specifies a clockwise rotation and a negative number specifies a counterclockwise rotation.


### -param sweepDirection [in]

Type: <b><a href="https://msdn.microsoft.com/97e6f384-7a42-4852-b948-66010bffed22">D2D1_SWEEP_DIRECTION</a></b>

A value that specifies whether the arc sweep is clockwise or counterclockwise.




### -param arcSize [in]

Type: <b><a href="https://msdn.microsoft.com/c471716d-c2cc-4f79-8011-46690812b848">D2D1_ARC_SIZE</a></b>

A value  that specifies whether the arc is larger than 180 degrees.


## -returns



Type: <b><a href="https://msdn.microsoft.com/3f391265-20b4-4897-aa0b-d14b71cd5f0a">D2D1_ARC_SEGMENT</a></b>

The new arc segment.






## -see-also




<a href="https://msdn.microsoft.com/6d2c1959-1309-45d8-8204-19ffea03375b">ID2D1GeometrySink</a>
 

 

