---
UID: NF:shlwapi.ColorRGBToHLS
title: ColorRGBToHLS function
author: windows-driver-content
description: Converts colors from RGB to hue-luminance-saturation (HLS) format.
old-location: shell\ColorRGBToHLS.htm
old-project: shell
ms.assetid: ed000f53-cc7e-4693-994c-a5dd7c789f1f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ColorRGBToHLS, ColorRGBToHLS function [Windows Shell], _win32_ColorRGBToHLS, shell.ColorRGBToHLS, shlwapi/ColorRGBToHLS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
-	api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
-	ColorRGBToHLS
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# ColorRGBToHLS function


## -description


Converts colors from RGB to hue-luminance-saturation (HLS) format.


## -parameters




### -param clrRGB

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

The original RGB color.


### -param pwHue [out]

Type: <b>WORD*</b>

A pointer to a value that, when this method returns successfully, receives the HLS hue value.


### -param pwLuminance [out]

Type: <b>WORD*</b>

A pointer to a value that, when this method returns successfully, receives the HLS luminance value.


### -param pwSaturation [out]

Type: <b>WORD*</b>

A pointer to a value that, when this method returns successfully, receives the HLS saturation value.


## -returns



This function does not return a value.



