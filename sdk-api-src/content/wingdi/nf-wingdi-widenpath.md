---
UID: NF:wingdi.WidenPath
title: WidenPath function
author: windows-sdk-content
description: The WidenPath function redefines the current path as the area that would be painted if the path were stroked using the pen currently selected into the given device context.
old-location: gdi\widenpath.htm
tech.root: gdi
ms.assetid: c994bd1b-c5e8-46e6-a6a6-59e2d9106d75
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: WidenPath, WidenPath function [Windows GDI], _win32_WidenPath, gdi.widenpath, wingdi/WidenPath
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
 - WidenPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WidenPath function


## -description


The <b>WidenPath</b> function redefines the current path as the area that would be painted if the path were stroked using the pen currently selected into the given device context.


## -parameters




### -param hdc [in]

A handle to a device context that contains a closed path.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>WidenPath</b> function is successful only if the current pen is a geometric pen created by the <a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a> function, or if the pen is created with the <a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a> function and has a width, in device units, of more than one.

The device context identified by the <i>hdc</i> parameter must contain a closed path.

Any Bézier curves in the path are converted to sequences of straight lines approximating the widened curves. As such, no Bézier curves remain in the path after <b>WidenPath</b> is called.




## -see-also




<a href="https://msdn.microsoft.com/88be3405-a420-4eb1-935b-099dc3067530">BeginPath</a>



<a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a>



<a href="https://msdn.microsoft.com/0b4daf81-d1d6-45c1-b081-855b7cd8527a">EndPath</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>



<a href="https://msdn.microsoft.com/4bed113b-9e3f-441f-96d7-71630bf9298e">SetMiterLimit</a>
 

 

