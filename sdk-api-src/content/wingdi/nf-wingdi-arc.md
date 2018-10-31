---
UID: NF:wingdi.Arc
title: Arc function
author: windows-sdk-content
description: The Arc function draws an elliptical arc.
old-location: gdi\arc.htm
tech.root: gdi
ms.assetid: c15a2173-0fad-4a8a-b0f9-cd39fe4e7bac
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: Arc, Arc function [Windows GDI], _win32_Arc, gdi.arc, wingdi/Arc
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - Arc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Arc function


## -description


The <b>Arc</b> function draws an elliptical arc.


## -parameters




### -param hdc [in]

A handle to the device context where drawing takes place.


### -param x1 [in]

The x-coordinate, in logical units, of the upper-left corner of the bounding rectangle.


### -param y1 [in]

The y-coordinate, in logical units, of the upper-left corner of the bounding rectangle.


### -param x2 [in]

The x-coordinate, in logical units, of the lower-right corner of the bounding rectangle.


### -param y2 [in]

The y-coordinate, in logical units, of the lower-right corner of the bounding rectangle.


### -param x3 [in]

The x-coordinate, in logical units, of the ending point of the radial line defining the starting point of the arc.


### -param y3 [in]

The y-coordinate, in logical units, of the ending point of the radial line defining the starting point of the arc.


### -param x4 [in]

The x-coordinate, in logical units, of the ending point of the radial line defining the ending point of the arc.


### -param y4 [in]

The y-coordinate, in logical units, of the ending point of the radial line defining the ending point of the arc.


## -returns



If the arc is drawn, the return value is nonzero.

If the arc is not drawn, the return value is zero.




## -remarks



The points (<i>nLeftRect</i>, <i>nTopRect</i>) and (<i>nRightRect</i>, <i>nBottomRect</i>) specify the bounding rectangle. An ellipse formed by the specified bounding rectangle defines the curve of the arc. The arc extends in the current drawing direction from the point where it intersects the radial from the center of the bounding rectangle to the (<i>nXStartArc</i>, <i>nYStartArc</i>) point. The arc ends where it intersects the radial from the center of the bounding rectangle to the (<i>nXEndArc</i>, <i>nYEndArc</i>) point. If the starting point and ending point are the same, a complete ellipse is drawn.

The arc is drawn using the current pen; it is not filled.

The current position is neither used nor updated by <b>Arc</b>.

Use the <a href="https://msdn.microsoft.com/6bf426cd-e028-4568-9e9a-aca58dd69732">GetArcDirection</a> and <a href="https://msdn.microsoft.com/cec31eb2-cc9d-4384-b973-dd4339b96ed0">SetArcDirection</a> functions to get and set the current drawing direction for a device context. The default drawing direction is counterclockwise.




## -see-also




<a href="https://msdn.microsoft.com/65c38da1-ab7d-4e80-83e3-ba1db66f8fd9">AngleArc</a>



<a href="https://msdn.microsoft.com/5e358a14-9f39-4267-9a44-c8bf05b5dfbb">ArcTo</a>



<a href="https://msdn.microsoft.com/d6752c47-96a5-4fac-a1bb-0611a91f03f9">Chord</a>



<a href="https://msdn.microsoft.com/9bec59dd-6bcb-498e-9ed2-ac641ecd7fa5">Ellipse</a>



<a href="https://msdn.microsoft.com/6bf426cd-e028-4568-9e9a-aca58dd69732">GetArcDirection</a>



<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/86daa936-b483-4432-aa32-0b9328ff76f9">Pie</a>



<a href="https://msdn.microsoft.com/cec31eb2-cc9d-4384-b973-dd4339b96ed0">SetArcDirection</a>
 

 

