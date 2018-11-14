---
UID: NF:wingdi.Polyline
title: Polyline function
author: windows-sdk-content
description: The Polyline function draws a series of line segments by connecting the points in the specified array.
old-location: gdi\polyline.htm
tech.root: gdi
ms.assetid: 55481dd0-3db7-4131-b383-4d0036943e60
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Polyline, Polyline function [Windows GDI], _win32_Polyline, gdi.polyline, wingdi/Polyline
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
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - Polyline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- Polyline
: 
---

# Polyline function


## -description


The <b>Polyline</b> function draws a series of line segments by connecting the points in the specified array.


## -parameters




### -param hdc [in]

A handle to a device context.


### -param apt [in]

A pointer to an array of <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structures, in logical units.


### -param cpt [in]

The number of points in the array. This number must be greater than or equal to two.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The lines are drawn from the first point through subsequent points by using the current pen. Unlike the <a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a> or <a href="https://msdn.microsoft.com/76020742-b651-4244-82c3-13034573c306">PolylineTo</a> functions, the <b>Polyline</b> function neither uses nor updates the current position.




## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/71a9273f-321b-4efb-ac73-5979f8151d05">PolyPolyline</a>



<a href="https://msdn.microsoft.com/76020742-b651-4244-82c3-13034573c306">PolylineTo</a>
 

 

