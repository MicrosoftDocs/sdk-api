---
UID: NF:d2d1_1helper.BitmapProperties1
title: BitmapProperties1 function (d2d1_1helper.h)
description: Creates a D2D1_BITMAP_PROPERTIES1 structure.
helpviewer_keywords: ["BitmapProperties1","BitmapProperties1 function [Direct2D]","d2d1_1helper/BitmapProperties1","direct2d.bitmapproperties1"]
old-location: direct2d\bitmapproperties1.htm
tech.root: Direct2D
ms.assetid: 68391380-4C53-41EA-8458-EFD4387396D3
ms.date: 12/05/2018
ms.keywords: BitmapProperties1, BitmapProperties1 function [Direct2D], d2d1_1helper/BitmapProperties1, direct2d.bitmapproperties1
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
 - BitmapProperties1
 - d2d1_1helper/BitmapProperties1
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
 - BitmapProperties1
---

# BitmapProperties1 function


## -description

Creates a <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a> structure.

## -parameters

### -param bitmapOptions

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options">D2D1_BITMAP_OPTIONS</a></b>

A combination of <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options">D2D1_BITMAP_OPTIONS</a>-typed values that specify how the bitmap can be used.

### -param pixelFormat [in]

Type: <b>const <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a></b>

The bitmap's pixel format and alpha mode. The default value is a <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a> with a <b>format</b> of <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_UNKNOWN</a> and an <b>alphaMode</b> of  <a href="/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_UNKNOWN</a>. For more information about pixel formats, see <a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>.

### -param dpiX

Type: <b>FLOAT</b>

The horizontal dpi of the bitmap. The default value is 96.0f.

### -param dpiY

Type: <b>FLOAT</b>

The vertical dpi of the bitmap. The default value is 96.0f.

### -param colorContext [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>*</b>

An optional pointer to the <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a> interface for a color context to use with the bitmap. If you don't want to specify a color context, set this parameter to <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a></b>

A <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a> structure that describes the bitmap.