---
UID: NF:d2d1_1helper.ConvertColorSpace
title: ConvertColorSpace function (d2d1_1helper.h)
description: Convert a D2D1_COLOR_F from one color space to another.
helpviewer_keywords: ["ConvertColorSpace","ConvertColorSpace function [Direct2D]","d2d1_1helper/ConvertColorSpace","direct2d.convertcolorspace"]
old-location: direct2d\convertcolorspace.htm
tech.root: Direct2D
ms.assetid: 979E6FC2-52EB-4D58-B05C-523243F05B71
ms.date: 12/05/2018
ms.keywords: ConvertColorSpace, ConvertColorSpace function [Direct2D], d2d1_1helper/ConvertColorSpace, direct2d.convertcolorspace
req.header: d2d1_1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ConvertColorSpace
 - d2d1_1helper/ConvertColorSpace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ConvertColorSpace
---

# ConvertColorSpace function


## -description

Convert a <a href="/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a> from one color space to another.

## -parameters

### -param sourceColorSpace

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a></b>

The color space of the input.

### -param destinationColorSpace

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a></b>

The desired color space of the output.

### -param color [ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a></b>

The input color.

## -returns

Type: <b><a href="/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a></b>

The converted color in the new color space.