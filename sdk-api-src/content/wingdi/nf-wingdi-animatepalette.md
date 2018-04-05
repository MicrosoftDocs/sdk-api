---
UID: NF:wingdi.AnimatePalette
title: AnimatePalette function
author: windows-driver-content
description: The AnimatePalette function replaces entries in the specified logical palette.
old-location: gdi\animatepalette.htm
old-project: gdi
ms.assetid: 65dd45e2-39a4-4a94-bd14-b0c8e4a609a3
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: AnimatePalette, AnimatePalette function [Windows GDI], _win32_AnimatePalette, gdi.animatepalette, wingdi/AnimatePalette
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
req.typenames: FAX_TIME, *PFAX_TIME
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
-	AnimatePalette
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# AnimatePalette function


## -description


The <b>AnimatePalette</b> function replaces entries in the specified logical palette.


## -parameters




### -param hPal

TBD


### -param iStartIndex [in]

The first logical palette entry to be replaced.


### -param cEntries [in]

The number of entries to be replaced.


### -param ppe [in]

A pointer to the first member in an array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures used to replace the current entries.


#### - hpal [in]

A handle to the logical palette.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



An application can determine whether a device supports palette operations by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

The <b>AnimatePalette</b> function only changes entries with the PC_RESERVED flag set in the corresponding <b>palPalEntry</b> member of the <a href="https://msdn.microsoft.com/99d70a0e-ac61-4a88-a500-66443e7882ad">LOGPALETTE</a> structure.

If the given palette is associated with the active window, the colors in the palette are replaced immediately.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/f3462198-9360-4b77-ac62-9fe21ec666be">CreatePalette</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/99d70a0e-ac61-4a88-a500-66443e7882ad">LOGPALETTE</a>



<a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a>
 

 

