---
UID: NF:wingdi.GetClipRgn
title: GetClipRgn function
author: windows-sdk-content
description: The GetClipRgn function retrieves a handle identifying the current application-defined clipping region for the specified device context.
old-location: gdi\getcliprgn.htm
tech.root: gdi
ms.assetid: 66c807b8-129f-40f2-b8d8-995e0a5e22e4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetClipRgn, GetClipRgn function [Windows GDI], _win32_GetClipRgn, gdi.getcliprgn, wingdi/GetClipRgn
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
 - ext-ms-win-gdi-clipping-l1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetClipRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClipRgn function


## -description


The <b>GetClipRgn</b> function retrieves a handle identifying the current application-defined clipping region for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param hrgn [in]

A handle to an existing region before the function is called. After the function returns, this parameter is a handle to a copy of the current clipping region.


## -returns



If the function succeeds and there is no clipping region for the given device context, the return value is zero. If the function succeeds and there is a clipping region for the given device context, the return value is 1. If an error occurs, the return value is -1.




## -remarks



An application-defined clipping region is a clipping region identified by the <a href="https://msdn.microsoft.com/7a4f0b9c-8588-4da8-a030-ed9d8b4ee08d">SelectClipRgn</a> function. It is not a clipping region created when the application calls the <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function.

If the function succeeds, the <i>hrgn</i> parameter is a handle to a copy of the current clipping region. Subsequent changes to this copy will not affect the current clipping region.




## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/de9e5786-63d8-47be-8522-e96d7c0f8634">Clipping Functions</a>



<a href="https://msdn.microsoft.com/9e966369-9988-4bfa-af37-b1bbb3488880">Clipping Overview</a>



<a href="https://msdn.microsoft.com/7a4f0b9c-8588-4da8-a030-ed9d8b4ee08d">SelectClipRgn</a>
 

 

