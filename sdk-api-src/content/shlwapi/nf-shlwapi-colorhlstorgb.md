---
UID: NF:shlwapi.ColorHLSToRGB
title: ColorHLSToRGB function (shlwapi.h)
description: Converts colors from hue-luminance-saturation (HLS) to RGB format.
helpviewer_keywords: ["ColorHLSToRGB","ColorHLSToRGB function [Windows Shell]","_win32_ColorHLSToRGB","shell.ColorHLSToRGB","shlwapi/ColorHLSToRGB"]
old-location: shell\ColorHLSToRGB.htm
tech.root: shell
ms.assetid: 1bf0b337-01de-4ce3-851f-d845866fb46f
ms.date: 12/05/2018
ms.keywords: ColorHLSToRGB, ColorHLSToRGB function [Windows Shell], _win32_ColorHLSToRGB, shell.ColorHLSToRGB, shlwapi/ColorHLSToRGB
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
 - ColorHLSToRGB
 - shlwapi/ColorHLSToRGB
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
 - ColorHLSToRGB
---

# ColorHLSToRGB function


## -description

Converts colors from hue-luminance-saturation (HLS) to RGB format.

## -parameters

### -param wHue

Type: <b>WORD</b>

The original HLS hue value.
Can range from 0 to 240.

### -param wLuminance

Type: <b>WORD</b>

The original HLS luminance value.
Can range from 0 to 240.

### -param wSaturation

Type: <b>WORD</b>

The original HLS saturation value.
Can range from 0 to 240.

## -returns

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

Returns the RGB value.