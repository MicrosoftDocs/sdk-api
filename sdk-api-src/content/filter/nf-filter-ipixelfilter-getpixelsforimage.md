---
UID: NF:filter.IPixelFilter.GetPixelsForImage
tech.root: search
title: IPixelFilter::GetPixelsForImage
ms.date: 01/15/2025
targetos: Windows
description: Implemented by a search filter to supply pixel data for the image being indexed.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: filter.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - filter.h
api_name:
 - IPixelFilter::GetPixelsForImage
f1_keywords:
 - IPixelFilter::GetPixelsForImage
 - filter/IPixelFilter::GetPixelsForImage
dev_langs:
 - c++
helpviewer_keywords:
 - GetPixelsForImage
---

## -description

Implemented by a search filter to supply pixel data for the image being indexed.

## -parameters

### -param scalingFactor [in]

A FLOAT specifying the scaling factor with which the image should be scaled before populating *pixelBuffer*.

### -param sourceRect [in]

A RECT specifying the region of the image for which pixels values should be included in *pixelBuffer*. If this value is nullptr, the entire image should be included.

### -param pixelBufferSize [in]

The expected size of *pixelBuffer*, in bytes.

### -param pixelBuffer [out]

The buffer containing the requested pixel values. This buffer is client-managed and must have the size specified in *pixelBufferSize*.

## -returns

This method can return one of these values.

| Return code | Description |
|-------------|-------------|
| S_OK     | Success |

## -remarks

The image data returned in *pixelBuffer* must be in the [IMAGE_PIXELFORMAT](ne-filter-image_pixelformat.md) format specified in the **Format** field of the [IMAGE_INFO](ns-filter-image_info.md) structure returned from the filter's implementation of [IPixelFilter::GetImageInfo](nf-filter-ipixelfilter-getimageinfo.md).

## -see-also



