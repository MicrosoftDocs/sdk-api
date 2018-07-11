---
UID: NC:wingdi.LINEDDAPROC
title: LINEDDAPROC
author: windows-sdk-content
description: The LineDDAProc function is an application-defined callback function used with the LineDDA function.
old-location: gdi\lineddaproc.htm
old-project: gdi
ms.assetid: 4a8b1120-4b0b-4029-8b49-4371c0627bba
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: LineDDAProc, LineDDAProc callback, LineDDAProc callback function [Windows GDI], _win32_LineDDAProc, gdi.lineddaproc, wingdi/LineDDAProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: FAX_TIME, *PFAX_TIME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wingdi.h
api_name:
 - LineDDAProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# LINEDDAPROC callback function


## -description


The <b>LineDDAProc</b> function is an application-defined callback function used with the <a href="https://msdn.microsoft.com/1400d947-324a-4921-9f65-f5d3a11005da">LineDDA</a> function. It is used to process coordinates. The <b>LINEDDAPROC</b> type defines a pointer to this callback function. <b>LineDDAProc</b> is a placeholder for the application-defined function name.


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



An application registers a <b>LineDDAProc</b> function by passing its address to the <a href="https://msdn.microsoft.com/1400d947-324a-4921-9f65-f5d3a11005da">LineDDA</a> function.




## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/1400d947-324a-4921-9f65-f5d3a11005da">LineDDA</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>
 

 

