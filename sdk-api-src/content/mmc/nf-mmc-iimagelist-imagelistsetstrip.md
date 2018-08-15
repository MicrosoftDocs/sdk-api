---
UID: NF:mmc.IImageList.ImageListSetStrip
title: IImageList::ImageListSetStrip
author: windows-sdk-content
description: The IImageList::ImageListSetStrip method enables a user to add a strip of icons to the image list using a pair of bitmaps (large and small icons), starting at a location identified by nStartLoc.
old-location: mmc\iimagelist_imagelistsetstrip.htm
old-project: MMC
ms.assetid: b736a5ab-86a7-4c8d-82b7-bbe9f98bc402
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IImageList interface [MMC],ImageListSetStrip method, IImageList.ImageListSetStrip, IImageList::ImageListSetStrip, ImageListSetStrip, ImageListSetStrip method [MMC], ImageListSetStrip method [MMC],IImageList interface, _slate_iimagelist_imagelistsetstrip, mmc.iimagelist_imagelistsetstrip, mmc/IImageList::ImageListSetStrip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IImageList.ImageListSetStrip
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IImageList::ImageListSetStrip


## -description


The <b>IImageList::ImageListSetStrip</b> method enables a user to add a strip of icons to the image list using a pair of bitmaps (large and small icons), starting at a location identified by nStartLoc.


## -parameters




### -param pBMapSm




### -param pBMapLg




### -param nStartLoc [in]

A value that specifies the index assigned to the first image in the strip. This is a virtual index that is internally mapped to the actual index.


### -param cMask [in]

A value that specifies the color used to generate a mask.


#### - BMapLg [in]

Win32 HBITMAP handle to the large (32x32) icon image strip. The snap-in owns this resource and must free it when finished. A resource memory leak will occur if the snap-in does not free BMapLg.


#### - BMapSm [in]

Win32 HBITMAP handle to the small (16x16) icon image strip. The snap-in owns this resource and must free it when finished. A resource memory leak will occur if the snap-in does not free BMapSm.


## -returns



This method can return one of these values.




## -remarks



Both small and large bitmaps must be provided and the number of icons in each strip must be equal. The small bitmap must be 16 pixels high and 16*n pixels wide, where n is an integer value. The large bitmap must be 32 pixels high and 32*n pixels wide.

Each pixel of the color used to generate a mask in the specified bitmap is changed to black and the corresponding bit in the mask is set to one.




## -see-also




<a href="https://msdn.microsoft.com/a957239b-6cb2-4101-adeb-e9ba4f876af4">IImageList</a>
 

 

