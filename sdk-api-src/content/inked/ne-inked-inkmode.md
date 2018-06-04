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

# InkMode enumeration


## -description



Specifies the collection mode for drawn ink-whether ink collection is disabled, ink is collected, or ink and gestures are collected.




## -enum-fields




### -field IEM_Disabled


### -field IEM_Ink


### -field IEM_InkAndGesture




#### - IM_Disabled

Ink collection is disabled. No strokes are created when in this mode.


#### - IM_Ink

Ink only is collected, creating a stroke.


#### - IM_InkAndGesture

Default. Ink is collected and single-stroke gestures are accepted.


## -see-also




<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit Control Reference</a>



<a href="https://msdn.microsoft.com/26023012-9ab1-4bd9-beff-41587bc74f5e">InkEdit Messages</a>



<a href="https://msdn.microsoft.com/0e395907-108b-40cf-819b-65a34e4ffc4d">InkEdit::InkMode Property</a>
 

 

