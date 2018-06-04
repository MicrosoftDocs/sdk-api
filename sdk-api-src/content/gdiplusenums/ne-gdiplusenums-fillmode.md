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

# FillMode enumeration


## -description


The <b>FillMode</b> enumeration specifies how to fill areas that are formed when a path or curve intersects itself. This enumeration is used by several methods of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> class, including 
			<a href="https://msdn.microsoft.com/378f0d34-7328-45e5-9f55-826bdaed3aab">FillClosedCurve</a> and 
			<a href="https://msdn.microsoft.com/e7cc93ab-c1e6-40e7-8888-f6bbffa42a00">FillPolygon</a>, and by the constructors of the 
			<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> class.


## -enum-fields




### -field FillModeAlternate

Specifies that areas are filled according to the even-odd parity rule. According to this rule, you can determine whether a test point is inside or outside a closed curve as follows: Draw a line from the test point to a point that is distant from the curve. If that line crosses the curve an odd number of times, the test point is inside the curve; otherwise, the test point is outside the curve. 


### -field FillModeWinding

Specifies that areas are filled according to the nonzero winding rule. According to this rule, you can determine whether a test point is inside or outside a closed curve as follows: Draw a line from a test point to a point that is distant from the curve. Count the number of times the curve crosses the test line from left to right, and count the number of times the curve crosses the test line from right to left. If those two numbers are the same, the test point is outside the curve; otherwise, the test point is inside the curve. 


## -see-also




<a href="https://msdn.microsoft.com/378f0d34-7328-45e5-9f55-826bdaed3aab">FillClosedCurve Methods</a>



<a href="https://msdn.microsoft.com/e7cc93ab-c1e6-40e7-8888-f6bbffa42a00">FillPolygon Methods</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/933dd879-480c-4b8a-965a-1656382d849a">GraphicsPath Constructors</a>
 

 

