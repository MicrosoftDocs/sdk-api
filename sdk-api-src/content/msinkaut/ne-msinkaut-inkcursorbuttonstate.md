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

# InkCursorButtonState enumeration


## -description



Defines values that specify the state of a cursor button.




## -enum-fields




### -field ICBS_Unavailable


### -field ICBS_Up

The cursor button is up. A button on a pen tip is up when the pen is not pressed against the digitizer. A button on a pen barrel is up when the button is not depressed.


### -field ICBS_Down

The cursor button is down. A button on a pen tip is down when the user lowers the pen to the digitizer and draws a stroke. For a button on a barrel, the button is down when the button is depressed.


#### - ICBS_CursorUnavailable

The cursor button is unavailable. A cursor button may become unavailable, for example, when a cursor leaves the range of Tablet PC.


## -remarks



The CursorButton state for the mouse is always <b>CursorUnavailable</b> when the mouse buttons are up.




## -see-also




<a href="https://msdn.microsoft.com/d05b240c-ba64-4008-b25d-e06c052eb5b0">CursorInRange Event</a>



<a href="https://msdn.microsoft.com/166bffdc-ec72-427a-a4bd-35ff16e8eb60">State Property</a>
 

 

