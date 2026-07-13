---
UID: NS:filter.IMAGE_INFO
tech.root: search
title: IMAGE_INFO
ms.date: 01/15/2025
targetos: Windows
description: Represents image metadata, including dimensions and format. This structure is populated by a search filter and returned from its implementation of IPixelFilter::GetImageInfo.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: filter.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: IMAGE_INFO
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - filter.h
api_name:
 - IMAGE_INFO
f1_keywords:
 - IMAGE_INFO
 - filter/IMAGE_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - IMAGE_INFO
---

## -description

Represents image metadata, including dimensions and format. This structure is populated by a search filter and returned from its implementation of [IPixelFilter::GetImageInfo](nf-filter-ipixelfilter-getimageinfo.md).

## -struct-fields

### -field Width

The width of the image being indexed, in pixels.

### -field Height

The height of the image being indexed, in pixels.

### -field Format

A member of the [IMAGE_PIXELFORMAT](ne-filter-image_pixelformat.md) enumeration, specifying the format of the image being indexed.

## -remarks

## -see-also

