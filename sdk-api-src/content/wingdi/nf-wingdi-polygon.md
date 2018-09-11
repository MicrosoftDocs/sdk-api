---
UID: NF:wingdi.Polygon
title: Polygon function
author: windows-sdk-content
description: The Polygon function draws a polygon consisting of two or more vertices connected by straight lines. The polygon is outlined by using the current pen and filled by using the current brush and polygon fill mode.
old-location: gdi\polygon.htm
tech.root: gdi
ms.assetid: 2f958b91-039a-4e02-b727-be142bb18b06
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Polygon, Polygon function [Windows GDI], _win32_Polygon, gdi.polygon, wingdi/Polygon
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
 - Polygon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Polygon function


## -description


The <b>Polygon</b> function draws a polygon consisting of two or more vertices connected by straight lines. The polygon is outlined by using the current pen and filled by using the current brush and polygon fill mode.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param apt [in]

A pointer to an array of <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structures that specify the vertices of the polygon, in logical coordinates.


### -param cpt [in]

The number of vertices in the array. This value must be greater than or equal to 2.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The polygon is closed automatically by drawing a line from the last vertex to the first.

The current position is neither used nor updated by the <b>Polygon</b> function.

Any extra points are ignored. To draw a line with more points, divide your data into groups, each of which have less than the maximum number of points, and call the function for each group of points. Remember to connect the line segments.




## -see-also




<a href="https://msdn.microsoft.com/8909e85d-fa5b-4058-9e58-e027160ec381">Filled Shape Functions</a>



<a href="https://msdn.microsoft.com/78439288-a769-4aab-aee7-7a03396ccebc">Filled Shapes Overview</a>



<a href="https://msdn.microsoft.com/febf96fb-bf2e-4eb2-ab5f-89741a1decad">GetPolyFillMode
      </a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT
      </a>



<a href="https://msdn.microsoft.com/ac0a2802-c8b0-4cd7-9521-5b179f2c70b9">PolyPolygon
      </a>



<a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">Polyline
      </a>



<a href="https://msdn.microsoft.com/76020742-b651-4244-82c3-13034573c306">PolylineTo
      </a>



<a href="https://msdn.microsoft.com/233926c4-2658-405d-89b6-05ece844623d">SetPolyFillMode
      </a>
 

 

