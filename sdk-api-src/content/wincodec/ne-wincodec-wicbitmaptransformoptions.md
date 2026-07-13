---
UID: NE:wincodec.WICBitmapTransformOptions
title: WICBitmapTransformOptions (wincodec.h)
description: Specifies the flip and rotation transforms.
helpviewer_keywords: ["WICBitmapTransformFlipHorizontal","WICBitmapTransformFlipVertical","WICBitmapTransformOptions","WICBitmapTransformOptions enumeration [Windows Imaging Component]","WICBitmapTransformRotate0","WICBitmapTransformRotate180","WICBitmapTransformRotate270","WICBitmapTransformRotate90","_wic_codec_wicbitmaptransformoptions","wic._wic_codec_wicbitmaptransformoptions","wincodec/WICBitmapTransformFlipHorizontal","wincodec/WICBitmapTransformFlipVertical","wincodec/WICBitmapTransformOptions","wincodec/WICBitmapTransformRotate0","wincodec/WICBitmapTransformRotate180","wincodec/WICBitmapTransformRotate270","wincodec/WICBitmapTransformRotate90"]
old-location: wic\_wic_codec_wicbitmaptransformoptions.htm
tech.root: wic
ms.assetid: e123bb4d-bc75-4f3f-98f1-bea9b008498b
ms.date: 12/05/2018
ms.keywords: WICBitmapTransformFlipHorizontal, WICBitmapTransformFlipVertical, WICBitmapTransformOptions, WICBitmapTransformOptions enumeration [Windows Imaging Component], WICBitmapTransformRotate0, WICBitmapTransformRotate180, WICBitmapTransformRotate270, WICBitmapTransformRotate90, _wic_codec_wicbitmaptransformoptions, wic._wic_codec_wicbitmaptransformoptions, wincodec/WICBitmapTransformFlipHorizontal, wincodec/WICBitmapTransformFlipVertical, wincodec/WICBitmapTransformOptions, wincodec/WICBitmapTransformRotate0, wincodec/WICBitmapTransformRotate180, wincodec/WICBitmapTransformRotate270, wincodec/WICBitmapTransformRotate90
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
req.typenames: WICBitmapTransformOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICBitmapTransformOptions
 - wincodec/WICBitmapTransformOptions
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
 - WICBitmapTransformOptions
---

# WICBitmapTransformOptions enumeration


## -description

Specifies the flip and rotation transforms.

## -enum-fields

### -field WICBitmapTransformRotate0:0

A rotation of 0 degrees.

### -field WICBitmapTransformRotate90:0x1

A clockwise rotation of 90 degrees.

### -field WICBitmapTransformRotate180:0x2

A clockwise rotation of 180 degrees.

### -field WICBitmapTransformRotate270:0x3

A clockwise rotation of 270 degrees.

### -field WICBitmapTransformFlipHorizontal:0x8

A horizontal flip. Pixels are flipped around the vertical y-axis.

### -field WICBitmapTransformFlipVertical:0x10

A vertical flip. Pixels are flipped around the horizontal x-axis.

### -field WICBITMAPTRANSFORMOPTIONS_FORCE_DWORD:0x7fffffff

