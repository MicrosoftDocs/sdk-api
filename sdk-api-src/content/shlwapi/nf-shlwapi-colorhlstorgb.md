---
UID: NF:shlwapi.ColorHLSToRGB
title: ColorHLSToRGB function (shlwapi.h)
author: windows-sdk-content
description: Converts colors from hue-luminance-saturation (HLS) to RGB format.
old-location: shell\ColorHLSToRGB.htm
tech.root: shell
ms.assetid: 1bf0b337-01de-4ce3-851f-d845866fb46f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ColorHLSToRGB, ColorHLSToRGB function [Windows Shell], _win32_ColorHLSToRGB, shell.ColorHLSToRGB, shlwapi/ColorHLSToRGB
ms.topic: function
f1_keywords: 
 - "shlwapi/ColorHLSToRGB"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - ColorHLSToRGB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ColorHLSToRGB function


## -description


Converts colors from hue-luminance-saturation (HLS) to RGB format.


## -parameters




### -param wHue

Type: <b>WORD</b>

The original HLS hue value.


### -param wLuminance

Type: <b>WORD</b>

The original HLS luminance value.


### -param wSaturation

Type: <b>WORD</b>

The original HLS saturation value.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a></b>

Returns the RGB value.



