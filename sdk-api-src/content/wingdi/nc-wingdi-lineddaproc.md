---
UID: NC:wingdi.LINEDDAPROC
title: LINEDDAPROC (wingdi.h)
author: windows-sdk-content
description: The LineDDAProc function is an application-defined callback function used with the LineDDA function.
old-location: gdi\lineddaproc.htm
tech.root: gdi
ms.assetid: 4a8b1120-4b0b-4029-8b49-4371c0627bba
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LineDDAProc, LineDDAProc callback, LineDDAProc callback function [Windows GDI], _win32_LineDDAProc, gdi.lineddaproc, wingdi/LineDDAProc
ms.topic: callback
f1_keywords: 
 - "wingdi/LineDDAProc"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wingdi.h
api_name:
 - LineDDAProc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LINEDDAPROC callback function


## -description


The <b>LineDDAProc</b> function is an application-defined callback function used with the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-linedda">LineDDA</a> function. It is used to process coordinates. The <b>LINEDDAPROC</b> type defines a pointer to this callback function. <b>LineDDAProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - X [in]

Specifies the x-coordinate, in logical units, of the current point.


#### - Y [in]

Specifies the y-coordinate, in logical units, of the current point.


#### - lpData [in]

Pointer to the application-defined data.


## -returns



This function does not return a value.




## -remarks



An application registers a <b>LineDDAProc</b> function by passing its address to the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-linedda">LineDDA</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-linedda">LineDDA</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>
 

 

