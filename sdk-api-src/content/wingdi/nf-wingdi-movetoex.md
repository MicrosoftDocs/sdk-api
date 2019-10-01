---
UID: NF:wingdi.MoveToEx
title: MoveToEx function (wingdi.h)
author: windows-sdk-content
description: The MoveToEx function updates the current position to the specified point and optionally returns the previous position.
old-location: gdi\movetoex.htm
tech.root: gdi
ms.assetid: af11eeb7-4036-4a90-8685-9b5719f79e01
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MoveToEx, MoveToEx function [Windows GDI], _win32_MoveToEx, gdi.movetoex, wingdi/MoveToEx
ms.topic: function
f1_keywords: 
 - "wingdi/MoveToEx"
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
 - MoveToEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MoveToEx function


## -description


The <b>MoveToEx</b> function updates the current position to the specified point and optionally returns the previous position.


## -parameters




### -param hdc [in]

Handle to a device context.


### -param x [in]

Specifies the x-coordinate, in logical units, of the new position, in logical units.


### -param y [in]

Specifies the y-coordinate, in logical units, of the new position, in logical units.


### -param lppt [out]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure that receives the previous current position. If this parameter is a <b>NULL</b> pointer, the previous position is not returned.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>MoveToEx</b> function affects all drawing functions.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/gdi/drawing-markers">Drawing Markers</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-anglearc">AngleArc</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polybezierto">PolyBezierTo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-polylineto">PolylineTo</a>
 

 

