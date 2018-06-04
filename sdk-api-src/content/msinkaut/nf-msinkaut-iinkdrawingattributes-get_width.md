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

# IInkDrawingAttributes::get_Width


## -description



Gets or sets the y-axis dimension, or width, of the pen tip when drawing ink.



This property is read/write.


## -parameters


## -remarks



If the tablet reports pen pressure (if the <a href="https://msdn.microsoft.com/adf5beec-75df-46a3-91e4-33595340aca2">IgnorePressure</a> property is false), the actual width of the ink varies depending on the amount of pressure applied to the drawing surface. When maximum pressure is applied, the width is 150% of the value of the <code>Width</code> property. When minimum pressure is applied, the width is 50% of the value of the <code>Width</code> property. By default, this property is set to true, so that pressure from the pen is reported. To specify that pressure should not be reported (that the width of ink does not change), set the <b>IgnorePressure</b> property to true.

Precision is limited to one one-thousandth of a HIMETRIC unit (three digits to the right of the decimal point). For example, if you specify a value of 2.0006, the most precise measurement is 2.001.




## -see-also




<a href="https://msdn.microsoft.com/2dc9eb94-649f-42f6-8180-abf570bdc757">Height Property [InkDrawingAttributes Class]</a>



<a href="tablet.iinkdrawingattributes">IInkDrawingAttributes</a>



<a href="https://msdn.microsoft.com/adf5beec-75df-46a3-91e4-33595340aca2">IgnorePressure Property</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/13e3c2dc-99a4-4643-b8b2-48586b0eb2f0">PenTip Property</a>
 

 

