---
UID: NF:wingdi.ColorCorrectPalette
title: ColorCorrectPalette function
author: windows-sdk-content
description: The ColorCorrectPalette function corrects the entries of a palette using the WCS 1.0 parameters in the specified device context.
old-location: wcs\colorcorrectpalette.htm
old-project: WCS
ms.assetid: e7680521-fb1e-4292-945f-867964dac1ab
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: ColorCorrectPalette, ColorCorrectPalette function [Windows Color System], _color_ColorCorrectPalette, wcs.colorcorrectpalette, wingdi/ColorCorrectPalette
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: 
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
-	ColorCorrectPalette
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ColorCorrectPalette function


## -description


The <b>ColorCorrectPalette</b> function corrects the entries of a palette using the WCS 1.0 parameters in the specified device context.


## -parameters




### -param hdc

TBD


### -param hPal

TBD


### -param deFirst

TBD


### -param num

TBD




#### - dwFirstEntry

Specifies the first entry in the palette to be color corrected.


#### - dwNumOfEntries

Specifies the number of entries to color correct.


#### - hDC

Specifies a device context whose WCS parameters to use.


#### - hPalette

Specifies the handle to the palette to be color corrected.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

