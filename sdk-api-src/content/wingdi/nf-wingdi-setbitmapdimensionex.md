---
UID: NF:wingdi.SetBitmapDimensionEx
title: SetBitmapDimensionEx function
author: windows-sdk-content
description: The SetBitmapDimensionEx function assigns preferred dimensions to a bitmap. These dimensions can be used by applications; however, they are not used by the system.
old-location: gdi\setbitmapdimensionex.htm
tech.root: gdi
ms.assetid: 23960533-de71-4bff-a43f-75e5fe38fbec
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: SetBitmapDimensionEx, SetBitmapDimensionEx function [Windows GDI], _win32_SetBitmapDimensionEx, gdi.setbitmapdimensionex, wingdi/SetBitmapDimensionEx
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
 - SetBitmapDimensionEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetBitmapDimensionEx function


## -description


The <b>SetBitmapDimensionEx</b> function assigns preferred dimensions to a bitmap. These dimensions can be used by applications; however, they are not used by the system.


## -parameters




### -param hbm [in]

A handle to the bitmap. The bitmap cannot be a DIB-section bitmap.


### -param w [in]

The width, in 0.1-millimeter units, of the bitmap.


### -param h [in]

The height, in 0.1-millimeter units, of the bitmap.


### -param lpsz [out]

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure to receive the previous dimensions of the bitmap. This pointer can be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



An application can retrieve the dimensions assigned to a bitmap with the <b>SetBitmapDimensionEx</b> function by calling the <a href="https://msdn.microsoft.com/3e4f5afc-26d3-4fb2-8d00-183165fdf471">GetBitmapDimensionEx</a> function.

The bitmap identified by <i>hBitmap</i> cannot be a DIB section, which is a bitmap created by the <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a> function. If the bitmap is a DIB section, the <b>SetBitmapDimensionEx</b> function fails.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/3e4f5afc-26d3-4fb2-8d00-183165fdf471">GetBitmapDimensionEx</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>
 

 

