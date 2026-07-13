---
UID: NE:filter.IMAGE_PIXELFORMAT
tech.root: search
title: IMAGE_PIXELFORMAT
ms.date: 01/15/2025
targetos: Windows
description: Specifies the pixel format of an image. This enumeration is used with the IMAGE_INFO structure.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: filter.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11, version 26100
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
 - filter.h
api_name:
 - IMAGE_PIXELFORMAT
f1_keywords:
 - IMAGE_PIXELFORMAT
 - filter/IMAGE_PIXELFORMAT
dev_langs:
 - c++
helpviewer_keywords:
 - IMAGE_PIXELFORMAT
---

## -description

Specifies the pixel format of an image. This enumeration is used with the [IMAGE_INFO](ns-filter-image_info.md) structure.

## -enum-fields

### -field FILTER_PIXELFORMAT_BGRA8

The image format is 32 bits per pixel. This value corresponds to the Windows Imaging Component (WIC) friendly name **GUID_WICPixelFormat32bppBGRA**.

### -field FILTER_PIXELFORMAT_PBGRA8

The image format is 32 bits per pixel. This value corresponds to the WIC friendly name **GUID_WICPixelFormat32bppPBGRA**.

### -field FILTER_PIXELFORMAT_BGR8

The image format is 24 bits per pixel. This value corresponds to the WIC friendly name **GUID_WICPixelFormat24bppBGR**.

## -remarks

Specifying the bits per pixel (bpp) of an image allows a search indexer to allocate a buffer of the correct size to process the image. For more information on WIC pixel formats, see [Native pixel formats overview](/windows/win32/wic/-wic-codec-native-pixel-formats).

## -see-also

[IMAGE_INFO](ns-filter-image_info.md)

[Native pixel formats overview](/windows/win32/wic/-wic-codec-native-pixel-formats)
