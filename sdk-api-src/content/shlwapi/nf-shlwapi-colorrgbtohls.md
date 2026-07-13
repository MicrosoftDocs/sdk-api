---
UID: NF:shlwapi.ColorRGBToHLS
title: ColorRGBToHLS function (shlwapi.h)
description: Converts colors from RGB to hue-luminance-saturation (HLS) format.
helpviewer_keywords: ["ColorRGBToHLS","ColorRGBToHLS function [Windows Shell]","_win32_ColorRGBToHLS","shell.ColorRGBToHLS","shlwapi/ColorRGBToHLS"]
old-location: shell\ColorRGBToHLS.htm
tech.root: shell
ms.assetid: ed000f53-cc7e-4693-994c-a5dd7c789f1f
ms.date: 12/05/2018
ms.keywords: ColorRGBToHLS, ColorRGBToHLS function [Windows Shell], _win32_ColorRGBToHLS, shell.ColorRGBToHLS, shlwapi/ColorRGBToHLS
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
 - ColorRGBToHLS
 - shlwapi/ColorRGBToHLS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - ColorRGBToHLS
---

# ColorRGBToHLS function


## -description

Converts colors from RGB to hue-luminance-saturation (HLS) format.

## -parameters

### -param clrRGB

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

The original RGB color.

### -param pwHue [out]

Type: <b>WORD*</b>

A pointer to a value that, when this method returns successfully, receives the HLS hue value.
Can range from 0 to 240.

### -param pwLuminance [out]

Type: <b>WORD*</b>

A pointer to a value that, when this method returns successfully, receives the HLS luminance value.
Can range from 0 to 240.

### -param pwSaturation [out]

Type: <b>WORD*</b>

A pointer to a value that, when this method returns successfully, receives the HLS saturation value.
Can range from 0 to 240.