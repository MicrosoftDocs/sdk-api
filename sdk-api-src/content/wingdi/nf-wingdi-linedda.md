---
UID: NF:wingdi.LineDDA
title: LineDDA function
author: windows-sdk-content
description: The LineDDA function determines which pixels should be highlighted for a line defined by the specified starting and ending points.
old-location: gdi\linedda.htm
tech.root: gdi
ms.assetid: 1400d947-324a-4921-9f65-f5d3a11005da
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: LineDDA, LineDDA function [Windows GDI], _win32_LineDDA, gdi.linedda, wingdi/LineDDA
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
 - LineDDA
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Pointer to an application-defined callback function. For more information, see the <a href="https://msdn.microsoft.com/4a8b1120-4b0b-4029-8b49-4371c0627bba">LineDDAProc</a> callback function.


### -param data [in]

Pointer to the application-defined data.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>LineDDA</b> function passes the coordinates for each point along the line, except for the line's ending point, to the application-defined callback function. In addition to passing the coordinates of a point, this function passes any existing application-defined data.

The coordinates passed to the callback function match pixels on a video display only if the default transformations and mapping modes are used.




## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/4a8b1120-4b0b-4029-8b49-4371c0627bba">LineDDAProc</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>
 

 

