---
UID: NF:wingdi.ColorCorrectPalette
title: ColorCorrectPalette function (wingdi.h)
description: The ColorCorrectPalette function corrects the entries of a palette using the WCS 1.0 parameters in the specified device context.
old-location: wcs\colorcorrectpalette.htm
tech.root: WCS
ms.assetid: e7680521-fb1e-4292-945f-867964dac1ab
ms.date: 12/05/2018
ms.keywords: ColorCorrectPalette, ColorCorrectPalette function [Windows Color System], _color_ColorCorrectPalette, wcs.colorcorrectpalette, wingdi/ColorCorrectPalette
ms.topic: function
f1_keywords:
- wingdi/ColorCorrectPalette
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/previous-versions/dd316902(v=vs.85)">Functions</a>
 

 

