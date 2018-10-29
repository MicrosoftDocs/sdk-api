---
UID: NF:wingdi.GetMiterLimit
title: GetMiterLimit function
author: windows-sdk-content
description: The GetMiterLimit function retrieves the miter limit for the specified device context.
old-location: gdi\getmiterlimit.htm
tech.root: gdi
ms.assetid: 51b1fb95-dd44-47f8-9311-2c6dc9c57bbc
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetMiterLimit, GetMiterLimit function [Windows GDI], _win32_GetMiterLimit, gdi.getmiterlimit, wingdi/GetMiterLimit
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
 - GetMiterLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMiterLimit function


## -description


The <b>GetMiterLimit</b> function retrieves the miter limit for the specified device context.


## -parameters




### -param hdc [in]

Handle to the device context.


### -param plimit [out]

Pointer to a floating-point value that receives the current miter limit.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The miter limit is used when drawing geometric lines that have miter joins.




## -see-also




<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/68390601-1542-41dc-bea0-78f6c3318806">Path Functions</a>



<a href="https://msdn.microsoft.com/fbbd3ea0-9b35-4aaf-8498-187957e29cf0">Paths Overview</a>



<a href="https://msdn.microsoft.com/4bed113b-9e3f-441f-96d7-71630bf9298e">SetMiterLimit</a>
 

 

