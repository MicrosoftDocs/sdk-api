---
UID: NF:wingdi.PolylineTo
title: PolylineTo function
author: windows-sdk-content
description: The PolylineTo function draws one or more straight lines.
old-location: gdi\polylineto.htm
tech.root: gdi
ms.assetid: 76020742-b651-4244-82c3-13034573c306
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: PolylineTo, PolylineTo function [Windows GDI], _win32_PolylineTo, gdi.polylineto, wingdi/PolylineTo
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
api_name:
 - PolylineTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PolylineTo function


## -description


The <b>PolylineTo</b> function draws one or more straight lines.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param apt [in]

A pointer to an array of <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structures that contains the vertices of the line, in logical units.


### -param cpt [in]

The number of points in the array.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Unlike the <a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">Polyline</a> function, the <b>PolylineTo</b> function uses and updates the current position.

A line is drawn from the current position to the first point specified by the <i>lppt</i> parameter by using the current pen. For each additional line, the function draws from the ending point of the previous line to the next point specified by <i>lppt</i>.

<b>PolylineTo</b> moves the current position to the ending point of the last line.

If the line segments drawn by this function form a closed figure, the figure is not filled.




## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/71a9273f-321b-4efb-ac73-5979f8151d05">PolyPolyline</a>



<a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">Polyline</a>
 

 

