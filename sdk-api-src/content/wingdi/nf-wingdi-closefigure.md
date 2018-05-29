---
UID: NF:wingdi.CloseFigure
title: CloseFigure function
author: windows-sdk-content
description: The CloseFigure function closes an open figure in a path.
old-location: gdi\closefigure.htm
old-project: gdi
ms.assetid: 2532227c-35c9-4a46-b4eb-4a156ef28219
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CloseFigure, CloseFigure function [Windows GDI], _win32_CloseFigure, gdi.closefigure, wingdi/CloseFigure
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
-	Ext-MS-Win-GDI-Path-l1-1-0.dll
-	GDI32Full.dll
api_name:
-	CloseFigure
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CloseFigure function


## -description


The <b>CloseFigure</b> function closes an open figure in a path.


## -parameters




### -param hdc [in]

Handle to the device context in which the figure will be closed.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>CloseFigure</b> function closes the figure by drawing a line from the current position to the first point of the figure (usually, the point specified by the most recent call to the <a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a> function) and then connects the lines by using the line join style. If a figure is closed by using the <a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a> function instead of <b>CloseFigure</b>, end caps are used to create the corner instead of a join.

The <b>CloseFigure</b> function should only be called if there is an open path bracket in the specified device context.

A figure in a path is open unless it is explicitly closed by using this function. (A figure can be open even if the current point and the starting point of the figure are the same.)

After a call to <b>CloseFigure</b>, adding a line or curve to the path starts a new figure.




## -see-also




<a href="https://msdn.microsoft.com/88be3405-a420-4eb1-935b-099dc3067530">BeginPath</a>



<a href="https://msdn.microsoft.com/0b4daf81-d1d6-45c1-b081-855b7cd8527a">EndPath</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/a31b3a9a-110f-4cdf-89d9-19937a2e40b4">LineTo</a>



<a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>
 

 

