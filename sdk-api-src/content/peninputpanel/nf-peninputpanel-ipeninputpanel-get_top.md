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

# IPenInputPanel::get_Top


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Gets the vertical, or y-axis, location of the top edge of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object, in screen coordinates.



This property is read-only.


## -parameters


## -remarks



To explicitly override the automatic positioning behavior of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object, use the <a href="https://msdn.microsoft.com/99af3767-5bc9-43e3-9413-5886f057cb85">Left</a> and <b>Top</b> properties of the object to determine the current position of the pen input panel. If the pen input panel is located on a section of the screen that should be visible, use the <a href="https://msdn.microsoft.com/d99e5ef8-fa91-4507-bfe5-f30a039ca72d">MoveTo</a> method to relocate the pen input panel.

You can also override the automatic positioning behavior of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object by listening for the <i>Left</i> and <i>Top</i> parameters during a <a href="https://msdn.microsoft.com/0c51d875-cef9-4087-b17d-5c5af04f81a5">PanelMoving</a> event. If the pen input panel is located on a section of the screen that should be visible, use the <a href="https://msdn.microsoft.com/d99e5ef8-fa91-4507-bfe5-f30a039ca72d">MoveTo</a> method to relocate the pen input panel.




## -see-also




<a href="tablet.ipeninputpanel">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/99af3767-5bc9-43e3-9413-5886f057cb85">Left Property [PenInputPanel Class]</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

