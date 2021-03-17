---
UID: NF:d2d1_1.D2D1ConvertColorSpace
title: D2D1ConvertColorSpace function (d2d1_1.h)
description: Converts the given color from one colorspace to another.
helpviewer_keywords: ["D2D1ConvertColorSpace","D2D1ConvertColorSpace function [Direct2D]","d2d1_1/D2D1ConvertColorSpace","direct2d.d2d1convertcolorspace"]
old-location: direct2d\d2d1convertcolorspace.htm
tech.root: Direct2D
ms.assetid: ECFE9F50-290D-4E6C-90AB-A46B9E413A48
ms.date: 12/05/2018
ms.keywords: D2D1ConvertColorSpace, D2D1ConvertColorSpace function [Direct2D], d2d1_1/D2D1ConvertColorSpace, direct2d.d2d1convertcolorspace
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1ConvertColorSpace
 - d2d1_1/D2D1ConvertColorSpace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2D1.dll
api_name:
 - D2D1ConvertColorSpace
---

# D2D1ConvertColorSpace function


## -description

Converts the given color from one colorspace to another.

## -parameters

### -param sourceColorSpace

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a></b>

The source color space.

### -param destinationColorSpace

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a></b>

The destination color space.

### -param color [in]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a>*</b>

The source color.

## -returns

Type: <b><a href="/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a></b>

The converted color.