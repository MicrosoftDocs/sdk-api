---
UID: NE:wincodec.WICBitmapChainType
title: WICBitmapChainType
description: Defines constants that specify a type of chain.
ms.date: 07/16/2025
tech.root: wic
targetos: Windows
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: wincodec.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wincodec.h
api_name:
 - WICBitmapChainType
f1_keywords:
 - WICBitmapChainType
 - wincodec/WICBitmapChainType
dev_langs:
 - c++
helpviewer_keywords:
 - WICBitmapChainType
---

## -description

Defines constants that specify a type of chain. The frames that are in each chain don't need to have the same dimensions as the primary frame.

## -enum-fields

### -field WICBitmapChainType_Alternate:0x1

Specifies an ordered chain of alternate images. If the primary image can't be decoded or displayed (perhaps due to the use of an unsupported codec), then you can traverse the chain of alternate images until you find a frame that can be decoded. The alternate frames are ordered in decreasing order of preference. In other words, ordered with the most preferred (for example, highest quality) alternate frames listed first in the chain.

### -field WICBitmapChainType_Layer:0x2

Specifies an ordered chain of layer images, which are used to compose the primary image (referred to as a *layered image*). The images are stacked on top of a canvas, defined by the layered image, with the first image in the chain placed lowest in the stack. Alpha blending can be used to provide transparency between layers. The color of the canvas, and the coordinates at which each layer image should be placed, is defined as metadata accessible on the layered image. When you create a layered image, don't invoke **WritePixels** on the primary image because the primary image doesn't participate in the layering.

### -field WICBitmapChainType_Preview:0x3

Specifies an ordered chain of preview images, which can be displayed as placeholders while the primary image is decoded. The chain of preview images is ordered by increasing quality. In other words, with the lowest complexity (quickest to decode) preview image listed first in the chain.

### -field WICBitmapChainType_Thumbnail:0x4

Specifies an ordered chain of thumbnail images, which represent the primary image. The chain of thumbnail images is ordered by increasing size. In other words, the lowest resolution image is listed first in the chain.

### -field WICBitmapChainType_AlphaMap:0x5

Specifies a chain containing a single frame with an alpha plane bitmap. When combined with the primary image, it can allow for alpha blending of the primary image. Typically, there's only a single frame in this chain. There's no defined ordering in the case of multiple frames in this chain.

### -field WICBitmapChainType_DepthMap:0x6

Specifies a chain containing a single frame with a depth bitmap. When combined with the primary image, it provides depth information to the pixels in the primary image. Typically, there's only a single frame in this chain. There's no defined ordering in the case of multiple frames in this chain.

### -field WICBitmapChainType_GainMap:0x7

Specifies a chain containing a single frame with a *gain map*. When combined with the primary image, it provides information to convert the primary image from standard-dynamic-range (SDR) to high-dynamic-range (HDR), or vice versa. The ISO 21496-1 standard defines how to use and create such gain maps. Typically, there's only a single frame in this chain. There's no defined ordering in the case of multiple frames in this chain.

### -field WICBITMAPCHAINTYPE_FORCE_DWORD

## -remarks

## -see-also
