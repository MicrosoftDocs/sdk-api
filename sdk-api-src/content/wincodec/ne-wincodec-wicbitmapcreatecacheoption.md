---
UID: NE:wincodec.WICBitmapCreateCacheOption
title: WICBitmapCreateCacheOption (wincodec.h)
description: Specifies the desired cache usage.
helpviewer_keywords: ["WICBitmapCacheOnDemand","WICBitmapCacheOnLoad","WICBitmapCreateCacheOption","WICBitmapCreateCacheOption enumeration [Windows Imaging Component]","WICBitmapNoCache","_wic_codec_wicbitmapcreatecacheoption","wic._wic_codec_wicbitmapcreatecacheoption","wincodec/WICBitmapCacheOnDemand","wincodec/WICBitmapCacheOnLoad","wincodec/WICBitmapCreateCacheOption","wincodec/WICBitmapNoCache"]
old-location: wic\_wic_codec_wicbitmapcreatecacheoption.htm
tech.root: wic
ms.assetid: 121d394d-e818-44c5-bf44-3b01df61c780
ms.date: 12/05/2018
ms.keywords: WICBitmapCacheOnDemand, WICBitmapCacheOnLoad, WICBitmapCreateCacheOption, WICBitmapCreateCacheOption enumeration [Windows Imaging Component], WICBitmapNoCache, _wic_codec_wicbitmapcreatecacheoption, wic._wic_codec_wicbitmapcreatecacheoption, wincodec/WICBitmapCacheOnDemand, wincodec/WICBitmapCacheOnLoad, wincodec/WICBitmapCreateCacheOption, wincodec/WICBitmapNoCache
f1_keywords:
- wincodec/WICBitmapCreateCacheOption
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wincodec.h
api_name:
- WICBitmapCreateCacheOption
targetos: Windows
req.typenames: WICBitmapCreateCacheOption
req.redist: 
ms.custom: 19H1
---

# WICBitmapCreateCacheOption enumeration


## -description


Specifies the desired cache usage.


## -enum-fields




### -field WICBitmapNoCache

Do not cache the bitmap.


### -field WICBitmapCacheOnDemand

Cache the bitmap when needed.


### -field WICBitmapCacheOnLoad

Cache the bitmap at initialization.


### -field WICBITMAPCREATECACHEOPTION_FORCE_DWORD




## -remarks



The <b>CreateBitmap</b> of the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a> interface does not support WICBitmapNoCache when the <i>pixelFormat</i> is a native pixel format provided by Windows Imaging Component (WIC).



