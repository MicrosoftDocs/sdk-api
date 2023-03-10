---
UID: NS:d2d1.D2D1_BITMAP_PROPERTIES
title: D2D1_BITMAP_PROPERTIES (d2d1.h)
description: Describes the pixel format and dpi of a bitmap.
helpviewer_keywords: ["D2D1_BITMAP_PROPERTIES","D2D1_BITMAP_PROPERTIES structure [Direct2D]","d2d1/D2D1_BITMAP_PROPERTIES","direct2d.D2D1_BITMAP_PROPERTIES"]
old-location: direct2d\D2D1_BITMAP_PROPERTIES.htm
tech.root: Direct2D
ms.assetid: 050246fd-f91a-4a2a-858a-5f0447e3ecbf
ms.date: 12/05/2018
ms.keywords: D2D1_BITMAP_PROPERTIES, D2D1_BITMAP_PROPERTIES structure [Direct2D], d2d1/D2D1_BITMAP_PROPERTIES, direct2d.D2D1_BITMAP_PROPERTIES
req.header: d2d1.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_BITMAP_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BITMAP_PROPERTIES
 - d2d1/D2D1_BITMAP_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_BITMAP_PROPERTIES
---

# D2D1_BITMAP_PROPERTIES structure


## -description

Describes the pixel format and dpi 
    of a bitmap.

## -struct-fields

### -field pixelFormat

Type: <b><a href="/windows/win32/api/dcommon/ns-dcommon-d2d1_pixel_format">D2D1_PIXEL_FORMAT</a></b>

The bitmap's pixel format and alpha mode.

### -field dpiX

Type: <b>FLOAT</b>

The horizontal dpi of the bitmap.

### -field dpiY

Type: <b>FLOAT</b>

The vertical dpi of the bitmap.

