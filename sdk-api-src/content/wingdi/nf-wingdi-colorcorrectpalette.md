---
UID: NF:wingdi.ColorCorrectPalette
title: ColorCorrectPalette function (wingdi.h)
description: The ColorCorrectPalette function corrects the entries of a palette using the WCS 1.0 parameters in the specified device context.
helpviewer_keywords: ["ColorCorrectPalette","ColorCorrectPalette function [Windows Color System]","_color_ColorCorrectPalette","wcs.colorcorrectpalette","wingdi/ColorCorrectPalette"]
old-location: wcs\colorcorrectpalette.htm
tech.root: WCS
ms.assetid: e7680521-fb1e-4292-945f-867964dac1ab
ms.date: 12/05/2018
ms.keywords: ColorCorrectPalette, ColorCorrectPalette function [Windows Color System], _color_ColorCorrectPalette, wcs.colorcorrectpalette, wingdi/ColorCorrectPalette
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ColorCorrectPalette
 - wingdi/ColorCorrectPalette
dev_langs:
 - c++
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

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
