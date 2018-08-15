---
UID: NF:shlwapi.ColorHLSToRGB
title: ColorHLSToRGB function
author: windows-sdk-content
description: Converts colors from hue-luminance-saturation (HLS) to RGB format.
old-location: shell\ColorHLSToRGB.htm
old-project: shell
ms.assetid: 1bf0b337-01de-4ce3-851f-d845866fb46f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ColorHLSToRGB, ColorHLSToRGB function [Windows Shell], _win32_ColorHLSToRGB, shell.ColorHLSToRGB, shlwapi/ColorHLSToRGB
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: URL_SCHEME
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
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



Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

Returns the RGB value.



