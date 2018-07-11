---
UID: NE:gdiplusenums.FillMode
title: FillMode
author: windows-sdk-content
description: The FillMode enumeration specifies how to fill areas that are formed when a path or curve intersects itself.
old-location: gdiplus\_gdiplus_ENUM_FillMode.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\fillmode.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FillMode, FillMode enumeration [GDI+], FillModeAlternate, FillModeWinding, _gdiplus_ENUM_FillMode, gdiplus._gdiplus_ENUM_FillMode, gdiplusenums/FillMode, gdiplusenums/FillModeAlternate, gdiplusenums/FillModeWinding
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - FillMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
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
 

 

