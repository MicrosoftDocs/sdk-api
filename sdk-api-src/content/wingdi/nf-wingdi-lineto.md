---
UID: NF:wingdi.LineTo
title: LineTo function (wingdi.h)
author: windows-sdk-content
description: The LineTo function draws a line from the current position up to, but not including, the specified point.
old-location: gdi\lineto.htm
tech.root: gdi
ms.assetid: a31b3a9a-110f-4cdf-89d9-19937a2e40b4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LineTo, LineTo function [Windows GDI], _win32_LineTo, gdi.lineto, wingdi/LineTo
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
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - LineTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LineTo function


## -description


The <b>LineTo</b> function draws a line from the current position up to, but not including, the specified point.


## -parameters




### -param hdc [in]

Handle to a device context.


### -param x [in]

Specifies the x-coordinate, in logical units, of the line's ending point.


### -param y [in]

Specifies the y-coordinate, in logical units, of the line's ending point.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The line is drawn by using the current pen and, if the pen is a geometric pen, the current brush.

If <b>LineTo</b> succeeds, the current position is set to the specified ending point.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/69114875-f3e0-45e9-8e87-1f4e9de08db1">Drawing Markers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>



<a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">Polyline</a>



<a href="https://msdn.microsoft.com/76020742-b651-4244-82c3-13034573c306">PolylineTo</a>
 

 

