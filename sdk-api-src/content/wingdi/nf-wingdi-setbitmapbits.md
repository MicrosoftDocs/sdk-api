---
UID: NF:wingdi.SetBitmapBits
title: SetBitmapBits function
author: windows-driver-content
description: The SetBitmapBits function sets the bits of color data for a bitmap to the specified values.
old-location: gdi\setbitmapbits.htm
old-project: gdi
ms.assetid: 3cab12a6-c408-4552-bec0-5ecfd8374757
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: SetBitmapBits, SetBitmapBits function [Windows GDI], _win32_SetBitmapBits, gdi.setbitmapbits, wingdi/SetBitmapBits
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
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	SetBitmapBits
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetBitmapBits function


## -description


The <b>SetBitmapBits</b> function sets the bits of color data for a bitmap to the specified values.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a> function.</div><div> </div>

## -parameters




### -param hbm

TBD


### -param cb

TBD


### -param pvBits

TBD




#### - cBytes [in]

The number of bytes pointed to by the <i>lpBits</i> parameter.


#### - hbmp [in]

A handle to the bitmap to be set. This must be a compatible bitmap (DDB).


#### - lpBits [in]

A pointer to an array of bytes that contain color data for the specified bitmap.


## -returns



If the function succeeds, the return value is the number of bytes used in setting the bitmap bits.

If the function fails, the return value is zero.




## -remarks



The array identified by <i>lpBits</i> must be WORD aligned.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/72e8cc6b-d282-451e-b6ec-0473d2daea7c">GetBitmapBits</a>



<a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a>
 

 

