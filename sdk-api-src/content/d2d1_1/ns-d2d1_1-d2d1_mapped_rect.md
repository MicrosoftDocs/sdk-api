---
UID: NS:d2d1_1.D2D1_MAPPED_RECT
title: D2D1_MAPPED_RECT (d2d1_1.h)
description: Describes mapped memory from the ID2D1Bitmap1::Map API.
helpviewer_keywords: ["D2D1_MAPPED_RECT","D2D1_MAPPED_RECT structure [Direct2D]","PD2D1_MAPPED_RECT","PD2D1_MAPPED_RECT structure pointer [Direct2D]","d2d1_1/D2D1_MAPPED_RECT","d2d1_1/PD2D1_MAPPED_RECT","direct2d.d2d1_mapped_rect"]
old-location: direct2d\d2d1_mapped_rect.htm
tech.root: Direct2D
ms.assetid: 1cd81f1a-c39b-4975-a801-aa9444dde172
ms.date: 12/05/2018
ms.keywords: D2D1_MAPPED_RECT, D2D1_MAPPED_RECT structure [Direct2D], PD2D1_MAPPED_RECT, PD2D1_MAPPED_RECT structure pointer [Direct2D], d2d1_1/D2D1_MAPPED_RECT, d2d1_1/PD2D1_MAPPED_RECT, direct2d.d2d1_mapped_rect
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
req.typenames: D2D1_MAPPED_RECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_MAPPED_RECT
 - d2d1_1/D2D1_MAPPED_RECT
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
 - D2D1_MAPPED_RECT
---

# D2D1_MAPPED_RECT structure


## -description

 Describes mapped memory from the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map">ID2D1Bitmap1::Map</a> API.

## -struct-fields

### -field pitch

The size in bytes of an individual scanline in the bitmap.

### -field bits

The data inside the bitmap.

## -remarks

The mapped rectangle is used to map a rectangle into the caller's address space.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map">ID2D1Bitmap1::Map</a>