---
UID: NS:d2d1_1.D2D1_BITMAP_PROPERTIES1
title: D2D1_BITMAP_PROPERTIES1 (d2d1_1.h)
description: This structure allows a ID2D1Bitmap1 to be created with bitmap options and color context information available.
helpviewer_keywords: ["D2D1_BITMAP_PROPERTIES1","D2D1_BITMAP_PROPERTIES1 structure [Direct2D]","PD2D1_BITMAP_PROPERTIES1","PD2D1_BITMAP_PROPERTIES1 structure pointer [Direct2D]","d2d1_1/D2D1_BITMAP_PROPERTIES1","d2d1_1/PD2D1_BITMAP_PROPERTIES1","direct2d.d2d1_bitmap_properties1"]
old-location: direct2d\d2d1_bitmap_properties1.htm
tech.root: Direct2D
ms.assetid: c9371ce3-f6fc-4fe6-ada6-0aa64a8f29a2
ms.date: 12/05/2018
ms.keywords: D2D1_BITMAP_PROPERTIES1, D2D1_BITMAP_PROPERTIES1 structure [Direct2D], PD2D1_BITMAP_PROPERTIES1, PD2D1_BITMAP_PROPERTIES1 structure pointer [Direct2D], d2d1_1/D2D1_BITMAP_PROPERTIES1, d2d1_1/PD2D1_BITMAP_PROPERTIES1, direct2d.d2d1_bitmap_properties1
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2D1.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_BITMAP_PROPERTIES1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BITMAP_PROPERTIES1
 - d2d1_1/D2D1_BITMAP_PROPERTIES1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_BITMAP_PROPERTIES1
---

# D2D1_BITMAP_PROPERTIES1 structure


## -description

This structure allows a <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a> to be created with bitmap options and color context information available.

## -struct-fields

### -field pixelFormat

Type: <b><a href="/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a></b>

The DXGI format and alpha mode to create the bitmap with.

### -field dpiX

Type: <b>FLOAT</b>

The bitmap dpi in the x direction.

### -field dpiY

Type: <b>FLOAT</b>

The bitmap dpi in the y direction.

### -field bitmapOptions

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options">D2D1_BITMAP_OPTIONS</a></b>

The special creation options of the bitmap.

### -field colorContext

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>*</b>

The optionally specified color context information.

## -remarks

If both <b>dpiX</b> and <b>dpiY</b> are 0, the dpi of the bitmap will be set to the desktop dpi if the device context is a windowed context, or 96 dpi for any other device context.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1)">ID2D1DeviceContext::CreateBitmap</a>