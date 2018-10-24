---
UID: NF:wingdi.ColorCorrectPalette
title: ColorCorrectPalette function
author: windows-sdk-content
description: The ColorCorrectPalette function corrects the entries of a palette using the WCS 1.0 parameters in the specified device context.
old-location: wcs\colorcorrectpalette.htm
tech.root: WCS
ms.assetid: e7680521-fb1e-4292-945f-867964dac1ab
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ColorCorrectPalette, ColorCorrectPalette function [Windows Color System], _color_ColorCorrectPalette, wcs.colorcorrectpalette, wingdi/ColorCorrectPalette
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ColorCorrectPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ColorCorrectPalette function


## -description


The <b>ColorCorrectPalette</b> function corrects the entries of a palette using the WCS 1.0 parameters in the specified device context.


## -parameters




### -param hdc

Specifies a device context whose WCS parameters to use.


### -param hPal

Specifies the handle to the palette to be color corrected.


### -param deFirst

Specifies the first entry in the palette to be color corrected.


### -param num

Specifies the number of entries to color correct.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

