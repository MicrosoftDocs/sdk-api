---
UID: NF:wingdi.GetBitmapBits
title: GetBitmapBits function
author: windows-driver-content
description: The GetBitmapBits function copies the bitmap bits of a specified device-dependent bitmap into a buffer.
old-location: gdi\getbitmapbits.htm
old-project: gdi
ms.assetid: 72e8cc6b-d282-451e-b6ec-0473d2daea7c
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetBitmapBits, GetBitmapBits function [Windows GDI], _win32_GetBitmapBits, gdi.getbitmapbits, wingdi/GetBitmapBits
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Draw-l1-1-0.dll
-	Ext-MS-Win-GDI-Draw-l1-1-1.dll
-	ext-ms-win-gdi-draw-l1-1-2.dll
-	Ext-MS-Win-GDI-Draw-L1-1-3.dll
-	GDI32Full.dll
api_name:
-	GetBitmapBits
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetBitmapBits function


## -description


The <b>GetBitmapBits</b> function copies the bitmap bits of a specified device-dependent bitmap into a buffer.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a> function.</div><div> </div>

## -parameters




### -param hbit

TBD


### -param cb

TBD


### -param lpvBits [out]

A pointer to a buffer to receive the bitmap bits. The bits are stored as an array of byte values.


#### - cbBuffer [in]

The number of bytes to copy from the bitmap into the buffer.


#### - hbmp [in]

A handle to the device-dependent bitmap.


## -returns



If the function succeeds, the return value is the number of bytes copied to the buffer.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>
 

 

