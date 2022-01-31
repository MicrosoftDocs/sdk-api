---
UID: NE:wincodec.WICBitmapDitherType
title: WICBitmapDitherType (wincodec.h)
description: Specifies the type of dither algorithm to apply when converting between image formats.
helpviewer_keywords: ["WICBitmapDitherType","WICBitmapDitherType enumeration [Windows Imaging Component]","WICBitmapDitherTypeDualSpiral4x4","WICBitmapDitherTypeDualSpiral8x8","WICBitmapDitherTypeErrorDiffusion","WICBitmapDitherTypeNone","WICBitmapDitherTypeOrdered16x16","WICBitmapDitherTypeOrdered4x4","WICBitmapDitherTypeOrdered8x8","WICBitmapDitherTypeSolid","WICBitmapDitherTypeSpiral4x4","WICBitmapDitherTypeSpiral8x8","_wic_codec_wicbitmapdithertype","wic._wic_codec_wicbitmapdithertype","wincodec/WICBitmapDitherType","wincodec/WICBitmapDitherTypeDualSpiral4x4","wincodec/WICBitmapDitherTypeDualSpiral8x8","wincodec/WICBitmapDitherTypeErrorDiffusion","wincodec/WICBitmapDitherTypeNone","wincodec/WICBitmapDitherTypeOrdered16x16","wincodec/WICBitmapDitherTypeOrdered4x4","wincodec/WICBitmapDitherTypeOrdered8x8","wincodec/WICBitmapDitherTypeSolid","wincodec/WICBitmapDitherTypeSpiral4x4","wincodec/WICBitmapDitherTypeSpiral8x8"]
old-location: wic\_wic_codec_wicbitmapdithertype.htm
tech.root: wic
ms.assetid: e3fd8f37-8ea9-4cdb-853b-d5119b7afdc9
ms.date: 12/05/2018
ms.keywords: WICBitmapDitherType, WICBitmapDitherType enumeration [Windows Imaging Component], WICBitmapDitherTypeDualSpiral4x4, WICBitmapDitherTypeDualSpiral8x8, WICBitmapDitherTypeErrorDiffusion, WICBitmapDitherTypeNone, WICBitmapDitherTypeOrdered16x16, WICBitmapDitherTypeOrdered4x4, WICBitmapDitherTypeOrdered8x8, WICBitmapDitherTypeSolid, WICBitmapDitherTypeSpiral4x4, WICBitmapDitherTypeSpiral8x8, _wic_codec_wicbitmapdithertype, wic._wic_codec_wicbitmapdithertype, wincodec/WICBitmapDitherType, wincodec/WICBitmapDitherTypeDualSpiral4x4, wincodec/WICBitmapDitherTypeDualSpiral8x8, wincodec/WICBitmapDitherTypeErrorDiffusion, wincodec/WICBitmapDitherTypeNone, wincodec/WICBitmapDitherTypeOrdered16x16, wincodec/WICBitmapDitherTypeOrdered4x4, wincodec/WICBitmapDitherTypeOrdered8x8, wincodec/WICBitmapDitherTypeSolid, wincodec/WICBitmapDitherTypeSpiral4x4, wincodec/WICBitmapDitherTypeSpiral8x8
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICBitmapDitherType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICBitmapDitherType
 - wincodec/WICBitmapDitherType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICBitmapDitherType
---

# WICBitmapDitherType enumeration


## -description

Specifies the type of dither algorithm to apply when converting between image formats.

## -enum-fields

### -field WICBitmapDitherTypeNone:0

A solid color algorithm without dither.

### -field WICBitmapDitherTypeSolid:0

A solid color algorithm without dither.

### -field WICBitmapDitherTypeOrdered4x4:0x1

A 4x4 ordered dither algorithm.

### -field WICBitmapDitherTypeOrdered8x8:0x2

An 8x8 ordered dither algorithm.

### -field WICBitmapDitherTypeOrdered16x16:0x3

A 16x16 ordered dither algorithm.

### -field WICBitmapDitherTypeSpiral4x4:0x4

A 4x4 spiral dither algorithm.

### -field WICBitmapDitherTypeSpiral8x8:0x5

An 8x8 spiral dither algorithm.

### -field WICBitmapDitherTypeDualSpiral4x4:0x6

A 4x4 dual spiral dither algorithm.

### -field WICBitmapDitherTypeDualSpiral8x8:0x7

An 8x8 dual spiral dither algorithm.

### -field WICBitmapDitherTypeErrorDiffusion:0x8

An error diffusion algorithm.

### -field WICBITMAPDITHERTYPE_FORCE_DWORD:0x7fffffff

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicformatconverter-initialize">Initialize</a>
