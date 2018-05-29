---
UID: NF:wingdi.ArcTo
title: ArcTo function
author: windows-sdk-content
description: The ArcTo function draws an elliptical arc.
old-location: gdi\arcto.htm
old-project: gdi
ms.assetid: 5e358a14-9f39-4267-9a44-c8bf05b5dfbb
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ArcTo, ArcTo function [Windows GDI], _win32_ArcTo, gdi.arcto, wingdi/ArcTo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	ArcTo
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ArcTo function


## -description


The <b>ArcTo</b> function draws an elliptical arc.


## -parameters




### -param hdc [in]

A handle to the device context where drawing takes place.


### -param left

TBD


### -param top

TBD


### -param right

TBD


### -param bottom

TBD


### -param xr1

TBD


### -param yr1

TBD


### -param xr2

TBD


### -param yr2

TBD




#### - nBottomRect [in]

The y-coordinate, in logical units, of the lower-right corner of the bounding rectangle.


#### - nLeftRect [in]

The x-coordinate, in logical units, of the upper-left corner of the bounding rectangle.


#### - nRightRect [in]

The x-coordinate, in logical units, of the lower-right corner of the bounding rectangle.


#### - nTopRect [in]

The y-coordinate, in logical units, of the upper-left corner of the bounding rectangle.


#### - nXRadial1 [in]

The x-coordinate, in logical units, of the endpoint of the radial defining the starting point of the arc.


#### - nXRadial2 [in]

The x-coordinate, in logical units, of the endpoint of the radial defining the ending point of the arc.


#### - nYRadial1 [in]

The y-coordinate, in logical units, of the endpoint of the radial defining the starting point of the arc.


#### - nYRadial2 [in]

The y-coordinate, in logical units, of the endpoint of the radial defining the ending point of the arc.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



<b>ArcTo</b> is similar to the <a href="https://msdn.microsoft.com/c15a2173-0fad-4a8a-b0f9-cd39fe4e7bac">Arc</a> function, except that the current position is updated.

The points (<i>nLeftRect</i>, <i>nTopRect</i>) and (<i>nRightRect</i>, <i>nBottomRect</i>) specify the bounding rectangle. An ellipse formed by the specified bounding rectangle defines the curve of the arc. The arc extends counterclockwise from the point where it intersects the radial line from the center of the bounding rectangle to the (<i>nXRadial1</i>, <i>nYRadial1</i>) point. The arc ends where it intersects the radial line from the center of the bounding rectangle to the (<i>nXRadial2</i>, <i>nYRadial2</i>) point. If the starting point and ending point are the same, a complete ellipse is drawn.

A line is drawn from the current position to the starting point of the arc. If no error occurs, the current position is set to the ending point of the arc.

The arc is drawn using the current pen; it is not filled.




## -see-also




<a href="https://msdn.microsoft.com/65c38da1-ab7d-4e80-83e3-ba1db66f8fd9">AngleArc</a>



<a href="https://msdn.microsoft.com/c15a2173-0fad-4a8a-b0f9-cd39fe4e7bac">Arc</a>



<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/cec31eb2-cc9d-4384-b973-dd4339b96ed0">SetArcDirection</a>
 

 

