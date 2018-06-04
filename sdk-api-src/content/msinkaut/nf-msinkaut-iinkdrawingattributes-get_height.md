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

# IInkDrawingAttributes::get_Height


## -description



Gets or sets the height of the pen when drawing ink with the <a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes</a> object.



This property is read/write.


## -parameters


## -remarks



This property applies only to the <a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">Rectangle</a> pen tip. The value represents the height of the side of the rectangle. If using the <b>Ball</b> pen tip then the height of the pen tip is equal to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553316">Width</a> property, and the <b>Height</b> property is ignored.

Precision is limited to 1/1000 (three digits to the right of the decimal point). For example, if you specify a value of 2.0006, the most precise measurement is 2.001.




## -see-also




<a href="tablet.iinkdrawingattributes">IInkDrawingAttributes</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">InkPenTip Enumeration</a>



<a href="https://msdn.microsoft.com/13e3c2dc-99a4-4643-b8b2-48586b0eb2f0">PenTip Property</a>



<a href="https://msdn.microsoft.com/6069f9d3-061a-48ba-8161-86d6152d68f0">Width Property [InkDrawingAttributes Class]</a>
 

 

