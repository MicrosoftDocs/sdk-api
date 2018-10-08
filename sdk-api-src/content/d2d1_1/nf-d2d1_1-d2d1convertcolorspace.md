---
UID: NF:d2d1_1.D2D1ConvertColorSpace
title: D2D1ConvertColorSpace function
author: windows-sdk-content
description: Converts the given color from one colorspace to another.
old-location: direct2d\d2d1convertcolorspace.htm
tech.root: Direct2D
ms.assetid: ECFE9F50-290D-4E6C-90AB-A46B9E413A48
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: D2D1ConvertColorSpace, D2D1ConvertColorSpace function [Direct2D], d2d1_1/D2D1ConvertColorSpace, direct2d.d2d1convertcolorspace
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2D1.lib
req.dll: D2D1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2D1.dll
api_name:
 - D2D1ConvertColorSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D2D1ConvertColorSpace function


## -description


Converts the given color from one colorspace to another.


## -parameters




### -param sourceColorSpace

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh446992(v=VS.85).aspx">D2D1_COLOR_SPACE</a></b>

The source color space.


### -param destinationColorSpace

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh446992(v=VS.85).aspx">D2D1_COLOR_SPACE</a></b>

The destination color space.


### -param color [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dd368081(v=VS.85).aspx">D2D1_COLOR_F</a>*</b>

The source color.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368081(v=VS.85).aspx">D2D1_COLOR_F</a></b>

The converted color.



