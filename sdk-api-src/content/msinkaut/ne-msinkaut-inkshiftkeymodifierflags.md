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

# InkShiftKeyModifierFlags enumeration


## -description



Specifies which modifier key was pressed.




## -enum-fields




### -field IKM_Shift

The SHIFT key was used as a modifier.


### -field IKM_Control

The CTRL key was used as a modifier.


### -field IKM_Alt

The ALT key was used as a modifier.


## -remarks



In C++, explicit casting is required when trying to set more than one flag at a time. A compilation error occurs if explicit casting is not used.




## -see-also




<a href="https://msdn.microsoft.com/14b05b72-ae5d-416a-8ea5-9d9716c0967f">KeyDown Event [InkEdit Control]</a>



<a href="https://msdn.microsoft.com/973d99f2-df09-4315-aaab-72877272100b">KeyUp Event [InkEdit Control]</a>



<a href="https://msdn.microsoft.com/ff776b2b-7dd8-4d3d-b0f6-714b186d447e">MouseDown Event [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/b4c703da-0e4a-4d4c-9a6c-0e002344fb2f">MouseMove Event [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/049e1560-d4b2-4d34-9d54-2b45217001b2">MouseUp Event [InkOverlay Class]</a>



<a href="https://msdn.microsoft.com/f56a8af9-7618-4fa3-8dd5-aa81a7f817e4">MouseWheel Event [InkPicture Control]</a>
 

 

