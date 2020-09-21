---
UID: NF:wingdi.LineDDA
title: LineDDA function (wingdi.h)
description: The LineDDA function determines which pixels should be highlighted for a line defined by the specified starting and ending points.
helpviewer_keywords: ["LineDDA","LineDDA function [Windows GDI]","_win32_LineDDA","gdi.linedda","wingdi/LineDDA"]
old-location: gdi\linedda.htm
tech.root: gdi
ms.assetid: 1400d947-324a-4921-9f65-f5d3a11005da
ms.date: 12/05/2018
ms.keywords: LineDDA, LineDDA function [Windows GDI], _win32_LineDDA, gdi.linedda, wingdi/LineDDA
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LineDDA
 - wingdi/LineDDA
dev_langs:
 - c++
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
 - LineDDA
---

# LineDDA function


## -description

The <b>LineDDA</b> function determines which pixels should be highlighted for a line defined by the specified starting and ending points.

## -parameters

### -param xStart [in]

Specifies the x-coordinate, in logical units, of the line's starting point.

### -param yStart [in]

Specifies the y-coordinate, in logical units, of the line's starting point.

### -param xEnd [in]

Specifies the x-coordinate, in logical units, of the line's ending point.

### -param yEnd [in]

Specifies the y-coordinate, in logical units, of the line's ending point.

### -param lpProc [in]

Pointer to an application-defined callback function. For more information, see the <a href="/windows/desktop/api/wingdi/nc-wingdi-lineddaproc">LineDDAProc</a> callback function.

### -param data [in]

Pointer to the application-defined data.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>LineDDA</b> function passes the coordinates for each point along the line, except for the line's ending point, to the application-defined callback function. In addition to passing the coordinates of a point, this function passes any existing application-defined data.

The coordinates passed to the callback function match pixels on a video display only if the default transformations and mapping modes are used.

## -see-also

<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/api/wingdi/nc-wingdi-lineddaproc">LineDDAProc</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>