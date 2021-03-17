---
UID: NF:d2d1helper.BitmapProperties
title: BitmapProperties function (d2d1helper.h)
description: Creates a D2D1_BITMAP_PROPERTIES structure.
helpviewer_keywords: ["BitmapProperties","BitmapProperties function [Direct2D]","d2d1helper/BitmapProperties","direct2d.bitmapproperties"]
old-location: direct2d\bitmapproperties.htm
tech.root: Direct2D
ms.assetid: 5f85602a-3706-4cd6-8124-07e06be2d29c
ms.date: 12/05/2018
ms.keywords: BitmapProperties, BitmapProperties function [Direct2D], d2d1helper/BitmapProperties, direct2d.bitmapproperties
req.header: d2d1helper.h
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
 - BitmapProperties
 - d2d1helper/BitmapProperties
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
 - BitmapProperties
---

# BitmapProperties function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties">D2D1_BITMAP_PROPERTIES</a> structure.

## -parameters

### -param pixelFormat [ref]

Type: <b>const <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a></b>

The bitmap's pixel format and alpha mode. The default value is a <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a> with a <b>format</b> of <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_UNKNOWN</a> and an <b>alphaMode</b> of  <a href="/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_UNKNOWN</a>. For more information about pixel formats, see <a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>.

### -param dpiX

Type: <b>FLOAT</b>

The horizontal dpi of the bitmap. The default value is 96.0f.

### -param dpiY

Type: <b>FLOAT</b>

The vertical dpi of the bitmap. The default value is 96.0f.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties">D2D1_BITMAP_PROPERTIES</a></b>

A structure that describes the pixel format and dpi 
    of a bitmap.

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>