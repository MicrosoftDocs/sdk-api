---
UID: NC:winuser.GRAYSTRINGPROC
title: GRAYSTRINGPROC
author: windows-sdk-content
description: The OutputProc function is an application-defined callback function used with the GrayString function.
old-location: gdi\outputproc.htm
tech.root: gdi
ms.assetid: 4d9145d2-5be4-4da3-9d03-01ebd74e0d06
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GRAYSTRINGPROC, GRAYSTRINGPROC callback, GRAYSTRINGPROC callback function [Windows GDI], _win32_OutputProc, gdi.outputproc, winuser/GRAYSTRINGPROC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winuser.h
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
 - Winuser.h
api_name:
 - GRAYSTRINGPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GRAYSTRINGPROC callback function


## -description


The <b>OutputProc</b> function is an application-defined callback function used with the <a href="https://msdn.microsoft.com/b14b8c40-f97f-4e41-8d8d-687692acfda9">GrayString</a> function. It is used to draw a string. The <b>GRAYSTRINGPROC</b> type defines a pointer to this callback function. <b>OutputProc</b> is a placeholder for the application-defined or library-defined function name.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - cchData [in]

The length, in characters, of the string.


#### - hdc [in]

A handle to a device context with a bitmap of at least the width and height specified by the <i>nWidth</i> and <i>nHeight</i> parameters passed to <a href="https://msdn.microsoft.com/b14b8c40-f97f-4e41-8d8d-687692acfda9">GrayString</a>.


#### - lpData [in]

A pointer to the string to be drawn.


## -returns



If it succeeds, the callback function should return <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -remarks



The callback function must draw an image relative to the coordinates (0,0).




## -see-also




<a href="https://msdn.microsoft.com/b14b8c40-f97f-4e41-8d8d-687692acfda9">GrayString</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>
 

 

