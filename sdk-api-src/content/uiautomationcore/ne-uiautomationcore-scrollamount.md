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

# ScrollAmount enumeration


## -description


Contains values that specify the direction and distance to scroll.


## -enum-fields




### -field ScrollAmount_LargeDecrement

Scrolling is done in large decrements, equivalent to pressing the PAGE UP key or clicking on a blank part of a scroll bar. If one page up is not a relevant amount for the control and no scroll bar exists, the value represents an amount equal to the current visible window.


### -field ScrollAmount_SmallDecrement

Scrolling is done in small decrements, equivalent to pressing an arrow key or clicking the arrow button on a scroll bar.


### -field ScrollAmount_NoAmount

No scrolling is done. 


### -field ScrollAmount_LargeIncrement

Scrolling is done in large increments, equivalent to pressing the PAGE DOWN or PAGE UP key or clicking on a blank part of a scroll bar. 
			If one page is not a relevant amount for the control and no scroll bar exists, the value represents an amount equal to the current visible window.


### -field ScrollAmount_SmallIncrement

Scrolling is done in small increments, equivalent to pressing an arrow key or clicking the arrow 
			button on a scroll bar.


## -see-also




<a href="https://msdn.microsoft.com/55e1b899-aa9f-45eb-9cfa-d645ea659988">IScrollProvider</a>
 

 

