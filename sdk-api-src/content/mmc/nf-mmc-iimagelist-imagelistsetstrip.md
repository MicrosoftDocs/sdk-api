---
UID: NF:mmc.IImageList.ImageListSetStrip
title: IImageList::ImageListSetStrip (mmc.h)
description: The IImageList::ImageListSetStrip method enables a user to add a strip of icons to the image list using a pair of bitmaps (large and small icons), starting at a location identified by nStartLoc.
helpviewer_keywords: ["IImageList interface [MMC]","ImageListSetStrip method","IImageList.ImageListSetStrip","IImageList::ImageListSetStrip","ImageListSetStrip","ImageListSetStrip method [MMC]","ImageListSetStrip method [MMC]","IImageList interface","_slate_iimagelist_imagelistsetstrip","mmc.iimagelist_imagelistsetstrip","mmc/IImageList::ImageListSetStrip"]
old-location: mmc\iimagelist_imagelistsetstrip.htm
tech.root: mmc
ms.assetid: b736a5ab-86a7-4c8d-82b7-bbe9f98bc402
ms.date: 12/05/2018
ms.keywords: IImageList interface [MMC],ImageListSetStrip method, IImageList.ImageListSetStrip, IImageList::ImageListSetStrip, ImageListSetStrip, ImageListSetStrip method [MMC], ImageListSetStrip method [MMC],IImageList interface, _slate_iimagelist_imagelistsetstrip, mmc.iimagelist_imagelistsetstrip, mmc/IImageList::ImageListSetStrip
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImageList::ImageListSetStrip
 - mmc/IImageList::ImageListSetStrip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IImageList.ImageListSetStrip
---

# IImageList::ImageListSetStrip


## -description

The <b>IImageList::ImageListSetStrip</b> method enables a user to add a strip of icons to the image list using a pair of bitmaps (large and small icons), starting at a location identified by nStartLoc.

## -parameters

### -param pBMapSm [in]

Win32 HBITMAP handle to the small (16x16) icon image strip. The snap-in owns this resource and must free it when finished. A resource memory leak will occur if the snap-in does not free BMapSm.

### -param pBMapLg [in]

Win32 HBITMAP handle to the large (32x32) icon image strip. The snap-in owns this resource and must free it when finished. A resource memory leak will occur if the snap-in does not free BMapLg.

### -param nStartLoc [in]

A value that specifies the index assigned to the first image in the strip. This is a virtual index that is internally mapped to the actual index.

### -param cMask [in]

A value that specifies the color used to generate a mask.

## -returns

This method can return one of these values.

## -remarks

Both small and large bitmaps must be provided and the number of icons in each strip must be equal. The small bitmap must be 16 pixels high and 16*n pixels wide, where n is an integer value. The large bitmap must be 32 pixels high and 32*n pixels wide.

Each pixel of the color used to generate a mask in the specified bitmap is changed to black and the corresponding bit in the mask is set to one.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iimagelist">IImageList</a>