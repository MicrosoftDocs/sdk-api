---
UID: NF:shlwapi.ColorAdjustLuma
title: ColorAdjustLuma function (shlwapi.h)
description: Changes the luminance of a RGB value. Hue and saturation are not affected.
helpviewer_keywords: ["ColorAdjustLuma","ColorAdjustLuma function [Windows Shell]","_win32_ColorAdjustLuma","shell.ColorAdjustLuma","shlwapi/ColorAdjustLuma"]
old-location: shell\ColorAdjustLuma.htm
tech.root: shell
ms.assetid: d113ad59-cde4-4f11-b7f1-53b3fb69ec10
ms.date: 12/05/2018
ms.keywords: ColorAdjustLuma, ColorAdjustLuma function [Windows Shell], _win32_ColorAdjustLuma, shell.ColorAdjustLuma, shlwapi/ColorAdjustLuma
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ColorAdjustLuma
 - shlwapi/ColorAdjustLuma
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - ColorAdjustLuma
---

# ColorAdjustLuma function


## -description

Changes the luminance of a RGB value. Hue and saturation are not affected.

## -parameters

### -param clrRGB

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

The initial RGB value.

### -param n

Type: <b>int</b>

The luminance in units of 0.1 percent of the total range. For example, a value of <i>n</i> = 50 corresponds to 5 percent of the maximum luminance.

### -param fScale

Type: <b>BOOL</b>

If <i>fScale</i> is set to <b>TRUE</b>, <i>n</i> specifies how much to increment or decrement the current luminance. If <i>fScale</i> is set to <b>FALSE</b>, <i>n</i> specifies the absolute luminance.

## -returns

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

Returns the modified RGB value.

## -remarks

If <i>fScale</i> is set to <b>TRUE</b>, <i>n</i> can range from -1000 to +1000.

If <i>fScale</i> is set to <b>FALSE</b>, <i>n</i> can range from 0 to 1000. Available luminance values range from 0 to a maximum. If the requested value is negative or exceeds the maximum, the luminance will be set to either zero or the maximum value, respectively.