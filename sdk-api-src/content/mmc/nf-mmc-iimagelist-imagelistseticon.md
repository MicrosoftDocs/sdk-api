---
UID: NF:mmc.IImageList.ImageListSetIcon
title: IImageList::ImageListSetIcon (mmc.h)
description: The IImageList::ImageListSetIcon method enables a user to set an icon in the image list or to create an icon if it is not there.
helpviewer_keywords: ["IImageList interface [MMC]","ImageListSetIcon method","IImageList.ImageListSetIcon","IImageList::ImageListSetIcon","ImageListSetIcon","ImageListSetIcon method [MMC]","ImageListSetIcon method [MMC]","IImageList interface","_slate_iimagelist_imagelistseticon","mmc.iimagelist_imagelistseticon","mmc/IImageList::ImageListSetIcon"]
old-location: mmc\iimagelist_imagelistseticon.htm
tech.root: mmc
ms.assetid: 3bdb166e-e78a-41a8-9bb7-904d0462f976
ms.date: 12/05/2018
ms.keywords: IImageList interface [MMC],ImageListSetIcon method, IImageList.ImageListSetIcon, IImageList::ImageListSetIcon, ImageListSetIcon, ImageListSetIcon method [MMC], ImageListSetIcon method [MMC],IImageList interface, _slate_iimagelist_imagelistseticon, mmc.iimagelist_imagelistseticon, mmc/IImageList::ImageListSetIcon
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
 - IImageList::ImageListSetIcon
 - mmc/IImageList::ImageListSetIcon
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
 - IImageList.ImageListSetIcon
---

# IImageList::ImageListSetIcon


## -description

The <b>IImageList::ImageListSetIcon</b> method enables a user to set an icon in the image list or to create an icon if it is not there.

## -parameters

### -param pIcon [in]

A value that specifies the Win32
      HICON handle to the icon to set. The type must be cast as a pointer to a LONG_PTR. The snap-in owns this resource and must free it when finished. A resource memory leak will occur if the snap-in does not free Icon.

### -param nLoc [in]

A value that specifies the index assigned to the entry. This is a virtual index that is internally mapped to the actual index.

## -returns

This method can return one of these values.

## -remarks

If the index specified by <i>nLoc</i> has been used before, 
<b>ImageListSetIcon</b> replaces the icon stored at <i>nLoc</i>. If it has not been previously used, a new entry in the image list is added. The icon being inserted must have both the 32x32 and 16x16 pixel sizes defined.

<h3><a id="Selectively_Changing_the_Small_or_Large_Icon_in_an_Image_List"></a><a id="selectively_changing_the_small_or_large_icon_in_an_image_list"></a><a id="SELECTIVELY_CHANGING_THE_SMALL_OR_LARGE_ICON_IN_AN_IMAGE_LIST"></a>Selectively Changing the Small or Large Icon in an Image List</h3>
In MMC 1.2, two new macros are introduced to support changing only the small or large icon in an image list. The two macros, ILSI_LARGE_ICON and ILSI_SMALL_ICON, are applied to the <i>nLoc</i> parameter of 
<b>ImageListSetIcon</b>.

The ILSI_LARGE_ICON macro is used to change only the large icon at nLoc. The ILSI_SMALL_ICON macro is used to change only the small icon at nLoc.

To set different large and small icons, you can use either one of the two macros. The following code examples show these macros.

<h3><a id="Snippet_1"></a><a id="snippet_1"></a><a id="SNIPPET_1"></a>Snippet 1</h3>

```cpp
pImageList->ImageListSetIcon((LONG_PTR*) hLargeIcon, nLoc); // set both
pImageList->ImageListSetIcon((LONG_PTR*) hSmallIcon, ILSI_SMALL_ICON (nLoc)); // change small
```


<h3><a id="Snippet_2"></a><a id="snippet_2"></a><a id="SNIPPET_2"></a>Snippet 2</h3>

```cpp
pImageList->ImageListSetIcon((LONG_PTR*) hSmallIcon, nLoc); // set both
pImageList->ImageListSetIcon((LONG_PTR*) hLargeIcon, ILSI_LARGE_ICON (nLoc)); // change large
```


Before using either ILSI_LARGE_ICON or ILSI_SMALL_ICON, the snap-in must first insert an image at nLoc. The 
ImageListSetIcon method will fail if the ILSI_LARGE_ICON or ILSI_SMALL_ICON macro is used and nLoc does not refer to an existing image.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iimagelist">IImageList</a>