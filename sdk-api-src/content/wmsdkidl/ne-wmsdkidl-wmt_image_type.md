---
UID: NE:wmsdkidl.WMT_IMAGE_TYPE
title: WMT_IMAGE_TYPE (wmsdkidl.h)
description: The WMT_IMAGE_TYPE enumeration type defines the types of images that can be used for banner ads. This type is used as the value of the BannerImageType attribute.
helpviewer_keywords: ["WMT_IMAGE_TYPE","WMT_IMAGE_TYPE enumeration [windows Media Format]","WMT_IT_BITMAP","WMT_IT_GIF","WMT_IT_JPEG","WMT_IT_NONE","wmformat.wmt_image_type","wmsdkidl/WMT_IMAGE_TYPE","wmsdkidl/WMT_IT_BITMAP","wmsdkidl/WMT_IT_GIF","wmsdkidl/WMT_IT_JPEG","wmsdkidl/WMT_IT_NONE"]
old-location: wmformat\wmt_image_type.htm
tech.root: wmformat
ms.assetid: 727cfed7-d818-4c0f-9e9f-a35d9a8c195e
ms.date: 12/05/2018
ms.keywords: WMT_IMAGE_TYPE, WMT_IMAGE_TYPE enumeration [windows Media Format], WMT_IT_BITMAP, WMT_IT_GIF, WMT_IT_JPEG, WMT_IT_NONE, wmformat.wmt_image_type, wmsdkidl/WMT_IMAGE_TYPE, wmsdkidl/WMT_IT_BITMAP, wmsdkidl/WMT_IT_GIF, wmsdkidl/WMT_IT_JPEG, wmsdkidl/WMT_IT_NONE
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WMT_IMAGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMT_IMAGE_TYPE
 - wmsdkidl/WMT_IMAGE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_IMAGE_TYPE
---

# WMT_IMAGE_TYPE enumeration


## -description

The <b>WMT_IMAGE_TYPE</b> enumeration type defines the types of images that can be used for banner ads. This type is used as the value of the <a href="/windows/desktop/wmformat/bannerimagetype">BannerImageType</a> attribute.

## -enum-fields

### -field WMT_IT_NONE:0

There is no image. If a <a href="/windows/desktop/wmformat/bannerimagedata">BannerImageData</a> attribute in the file, it will be ignored.

### -field WMT_IT_BITMAP:1

The banner image is an uncompressed bitmap.

### -field WMT_IT_JPEG:2

The banner image uses JPEG encoding.

### -field WMT_IT_GIF:3

The banner image uses GIF encoding.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
