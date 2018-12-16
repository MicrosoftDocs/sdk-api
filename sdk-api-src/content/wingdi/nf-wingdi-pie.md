---
UID: NF:wingdi.Pie
title: Pie function
author: windows-sdk-content
description: The Pie function draws a pie-shaped wedge bounded by the intersection of an ellipse and two radials. The pie is outlined by using the current pen and filled by using the current brush.
old-location: gdi\pie.htm
tech.root: gdi
ms.assetid: 86daa936-b483-4432-aa32-0b9328ff76f9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Pie, Pie function [Windows GDI], _win32_Pie, gdi.pie, wingdi/Pie
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
 - Pie
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Pie function


## -description


The <b>Pie</b> function draws a pie-shaped wedge bounded by the intersection of an ellipse and two radials. The pie is outlined by using the current pen and filled by using the current brush.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param left [in]

The x-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.


### -param top [in]

The y-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.


### -param right [in]

The x-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.


### -param bottom [in]

The y-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.


### -param xr1 [in]

The x-coordinate, in logical coordinates, of the endpoint of the first radial.


### -param yr1 [in]

The y-coordinate, in logical coordinates, of the endpoint of the first radial.


### -param xr2 [in]

The x-coordinate, in logical coordinates, of the endpoint of the second radial.


### -param yr2 [in]

The y-coordinate, in logical coordinates, of the endpoint of the second radial.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The curve of the pie is defined by an ellipse that fits the specified bounding rectangle. The curve begins at the point where the ellipse intersects the first radial and extends counterclockwise to the point where the ellipse intersects the second radial.

The current position is neither used nor updated by the <b>Pie</b> function.




## -see-also




<a href="https://msdn.microsoft.com/65c38da1-ab7d-4e80-83e3-ba1db66f8fd9">AngleArc
      </a>



<a href="https://msdn.microsoft.com/c15a2173-0fad-4a8a-b0f9-cd39fe4e7bac">Arc
      </a>



<a href="https://msdn.microsoft.com/5e358a14-9f39-4267-9a44-c8bf05b5dfbb">ArcTo
      </a>



<a href="https://msdn.microsoft.com/d6752c47-96a5-4fac-a1bb-0611a91f03f9">Chord
      </a>



<a href="https://msdn.microsoft.com/8909e85d-fa5b-4058-9e58-e027160ec381">Filled Shape Functions</a>



<a href="https://msdn.microsoft.com/78439288-a769-4aab-aee7-7a03396ccebc">Filled Shapes Overview</a>
 

 

