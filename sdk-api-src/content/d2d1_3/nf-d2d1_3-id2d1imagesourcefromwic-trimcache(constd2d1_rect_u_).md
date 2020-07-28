---
UID: NF:d2d1_3.ID2D1ImageSourceFromWic.TrimCache(constD2D1_RECT_U&)
title: ID2D1ImageSourceFromWic::TrimCache(const D2D1_RECT_U &) (d2d1_3.h)
description: This method trims the populated regions of the image source cache to just the specified rectangle.
helpviewer_keywords: ["ID2D1ImageSourceFromWic interface [Direct2D]","TrimCache method","ID2D1ImageSourceFromWic.TrimCache","ID2D1ImageSourceFromWic.TrimCache(const D2D1_RECT_U &)","ID2D1ImageSourceFromWic::TrimCache","ID2D1ImageSourceFromWic::TrimCache(const D2D1_RECT_U &)","TrimCache","TrimCache method [Direct2D]","TrimCache method [Direct2D]","ID2D1ImageSourceFromWic interface","d2d1_3/ID2D1ImageSourceFromWic::TrimCache","direct2d.id2d1imagesourcefromwic_trimcache_2"]
old-location: direct2d\id2d1imagesourcefromwic_trimcache_2.htm
tech.root: Direct2D
ms.assetid: AAC04CD2-D59B-42F0-90C9-F230EECE2028
ms.date: 12/05/2018
ms.keywords: ID2D1ImageSourceFromWic interface [Direct2D],TrimCache method, ID2D1ImageSourceFromWic.TrimCache, ID2D1ImageSourceFromWic.TrimCache(const D2D1_RECT_U &), ID2D1ImageSourceFromWic::TrimCache, ID2D1ImageSourceFromWic::TrimCache(const D2D1_RECT_U &), TrimCache, TrimCache method [Direct2D], TrimCache method [Direct2D],ID2D1ImageSourceFromWic interface, d2d1_3/ID2D1ImageSourceFromWic::TrimCache, direct2d.id2d1imagesourcefromwic_trimcache_2
f1_keywords:
- d2d1_3/ID2D1ImageSourceFromWic.TrimCache
dev_langs:
- c++
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d2d1_3.dll
api_name:
- ID2D1ImageSourceFromWic.TrimCache
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1ImageSourceFromWic::TrimCache(const D2D1_RECT_U &)


## -description


This method trims the populated regions of the image source cache to just the specified rectangle.


## -parameters




### -param rectangleToPreserve [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-rect-u">D2D1_RECT_U</a></b>

Specifies the region of the image, in pixels, which should be preserved in the image source cache. 
          Regions which are outside of the rectangle are evicted from the cache. By default, this is an empty rectangle, 
          meaning that the entire image is evicted from the cache.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The provided region must be constructed to include the scale at which the image source will be drawn at.  These coordinates must be provided in local coordinates.  
      This means that they must be adjusted prior to calling the API according to the DPI and other relevant transforms, which can include the world transform and brush transforms.

This method will fail if on-demand caching was not requested when the image source was created.

As with <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-clearresources">ID2D1Device::ClearResources</a>, the caller can need to subsequently issue a D3D flush before memory usage is reduced.

This operation is only supported when the image source has been initialized using the D2D1_IMAGE_SOURCE_LOADING_OPTIONS_CACHE_ON_DEMAND option.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic">ID2D1ImageSourceFromWic</a>
 

 

