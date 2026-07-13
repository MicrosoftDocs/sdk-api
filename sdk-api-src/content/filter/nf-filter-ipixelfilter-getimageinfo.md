---
UID: NF:filter.IPixelFilter.GetImageInfo
tech.root: search
title: IPixelFilter::GetImageInfo
ms.date: 01/15/2025
targetos: Windows
description: Implemented by a search filter to provide information about the dimensions and format of the image being indexed.
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
 - IPixelFilter::GetImageInfo
f1_keywords:
 - IPixelFilter::GetImageInfo
 - filter/IPixelFilter::GetImageInfo
dev_langs:
 - c++
helpviewer_keywords:
 - GetImageInfo
---

## -description

Implemented by a search filter to provide information about the dimensions and format of the image being indexed.

## -parameters

### -param imageInfo [out]

An [IMAGE_INFO](ns-filter-image_info.md) structure specifying the dimensions and format of the image being indexed.

## -returns

This method can return one of these values.

| Return code | Description |
|-------------|-------------|
| S_OK     | Success |
| E_OUTOFMEMORY | Failed to allocate necessary memory. |


## -remarks

The indexer calls **GetImageInfo** first, in order to allocate the necessary buffers for the image. After this method returns, the indexer will call [IPixelFilter::GetPixelsForImage](nf-filter-ipixelfilter-getpixelsforimage.md) one or more times to retrieve the raw image pixels.

## -see-also

