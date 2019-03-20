---
UID: NF:wingdi.StrokePath
title: StrokePath function (wingdi.h)
author: windows-sdk-content
description: The StrokePath function renders the specified path by using the current pen.
old-location: gdi\strokepath.htm
tech.root: gdi
ms.assetid: 5a9f1509-0a69-4db8-8d74-9bf360aca64d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: StrokePath, StrokePath function [Windows GDI], _win32_StrokePath, gdi.strokepath, wingdi/StrokePath
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
 - StrokePath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StrokePath function


## -description


The <b>StrokePath</b> function renders the specified path by using the current pen.


## -parameters




### -param hdc [in]

Handle to a device context that contains the completed path.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The path, if it is to be drawn by <b>StrokePath</b>, must have been completed through a call to <a href="https://msdn.microsoft.com/0b4daf81-d1d6-45c1-b081-855b7cd8527a">EndPath</a>. Calling this function on a path for which <b>EndPath</b> has not been called will cause this function to fail and return zero.  Unlike other path drawing functions such as <a href="https://msdn.microsoft.com/936af9e5-707d-4d43-9035-e8239e3759a2">StrokeAndFillPath</a>, <b>StrokePath</b> will not attempt to close the path by drawing a straight line from the first point on the path to the last point on the path.




## -see-also




<a href="https://msdn.microsoft.com/88be3405-a420-4eb1-935b-099dc3067530">BeginPath</a>



<a href="https://msdn.microsoft.com/0b4daf81-d1d6-45c1-b081-855b7cd8527a">EndPath</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>
 

 

