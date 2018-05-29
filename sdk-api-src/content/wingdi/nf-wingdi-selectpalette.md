---
UID: NF:wingdi.SelectPalette
title: SelectPalette function
author: windows-sdk-content
description: The SelectPalette function selects the specified logical palette into a device context.
old-location: gdi\selectpalette.htm
old-project: gdi
ms.assetid: 1fc3356f-6fa3-444f-b224-b953acd2394b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SelectPalette, SelectPalette function [Windows GDI], _win32_SelectPalette, gdi.selectpalette, wingdi/SelectPalette
ms.prod: windows
ms.technology: windows-sdk
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
-	Ext-MS-Win-GDI-DC-l1-2-0.dll
-	ext-ms-win-gdi-dc-l1-2-1.dll
-	GDI32Full.dll
api_name:
-	SelectPalette
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SelectPalette function


## -description


The <b>SelectPalette</b> function selects the specified logical palette into a device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param hPal

TBD


### -param bForceBkgd

TBD




#### - bForceBackground [in]

Specifies whether the logical palette is forced to be a background palette. If this value is <b>TRUE</b>, the <a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a> function causes the logical palette to be mapped to the colors already in the physical palette in the best possible way. This is always done, even if the window for which the palette is realized belongs to a thread without active focus.

If this value is <b>FALSE</b>, <a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a> causes the logical palette to be copied into the device palette when the application is in the foreground. (If the <i>hdc</i> parameter is a memory device context, this parameter is ignored.)


#### - hpal [in]

A handle to the logical palette to be selected.


## -returns



If the function succeeds, the return value is a handle to the device context's previous logical palette.

If the function fails, the return value is <b>NULL</b>.




## -remarks



An application can determine whether a device supports palette operations by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

An application can select a logical palette into more than one device context only if device contexts are compatible. Otherwise <b>SelectPalette</b> fails. To create a device context that is compatible with another device context, call <a href="https://msdn.microsoft.com/6ddc3705-2995-41af-af94-258aed597e17">CreateCompatibleDC</a> with the first device context as the parameter. If a logical palette is selected into more than one device context, changes to the logical palette will affect all device contexts for which it is selected.

An application might call the <b>SelectPalette</b> function with the <i>bForceBackground</i> parameter set to <b>TRUE</b> if the child windows of a top-level window each realize their own palettes. However, only the child window that needs to realize its palette must set <i>bForceBackground</i> to <b>TRUE</b>; other child windows must set this value to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/6ddc3705-2995-41af-af94-258aed597e17">CreateCompatibleDC</a>



<a href="https://msdn.microsoft.com/f3462198-9360-4b77-ac62-9fe21ec666be">CreatePalette</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a>
 

 

