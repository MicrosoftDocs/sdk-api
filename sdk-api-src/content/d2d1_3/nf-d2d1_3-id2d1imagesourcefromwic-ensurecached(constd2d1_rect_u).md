---
UID: NF:d2d1_3.ID2D1ImageSourceFromWic.EnsureCached(constD2D1_RECT_U)
title: ID2D1ImageSourceFromWic::EnsureCached(const D2D1_RECT_U) (d2d1_3.h)
description: Ensures that a specified region of the image source cache is populated. (overload 2/2)
helpviewer_keywords: ["EnsureCached","EnsureCached method [Direct2D]","EnsureCached method [Direct2D]","ID2D1ImageSourceFromWic interface","ID2D1ImageSourceFromWic interface [Direct2D]","EnsureCached method","ID2D1ImageSourceFromWic.EnsureCached","ID2D1ImageSourceFromWic.EnsureCached(const D2D1_RECT_U)","ID2D1ImageSourceFromWic::EnsureCached","ID2D1ImageSourceFromWic::EnsureCached(const D2D1_RECT_U)","d2d1_3/ID2D1ImageSourceFromWic::EnsureCached","direct2d.id2d1imagesourcefromwic_ensurecached"]
old-location: direct2d\id2d1imagesourcefromwic_ensurecached.htm
tech.root: Direct2D
ms.assetid: 3FF4E140-8318-4306-97EC-22BCCF69AD6E
ms.date: 12/05/2018
ms.keywords: EnsureCached, EnsureCached method [Direct2D], EnsureCached method [Direct2D],ID2D1ImageSourceFromWic interface, ID2D1ImageSourceFromWic interface [Direct2D],EnsureCached method, ID2D1ImageSourceFromWic.EnsureCached, ID2D1ImageSourceFromWic.EnsureCached(const D2D1_RECT_U), ID2D1ImageSourceFromWic::EnsureCached, ID2D1ImageSourceFromWic::EnsureCached(const D2D1_RECT_U), d2d1_3/ID2D1ImageSourceFromWic::EnsureCached, direct2d.id2d1imagesourcefromwic_ensurecached
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1ImageSourceFromWic::EnsureCached
 - d2d1_3/ID2D1ImageSourceFromWic::EnsureCached
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1ImageSourceFromWic.EnsureCached
---

# ID2D1ImageSourceFromWic::EnsureCached(const D2D1_RECT_U)


## -description

Ensures that a specified region of the image source cache is populated.
          This method can be used to minimize glitches by performing expensive work to populate caches outside of a rendering loop.
          This method can also be used to speculatively load image data before it is needed by drawing routines.

## -parameters

### -param rectangleToFill [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-u">D2D1_RECT_U</a>*</b>

Specifies the region of the image, in pixels, that should be populated in the cache. By default, this is the entire extent of the image.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This API loads image data into caches of image sources, if that data was not already cached.  It does not trim pre-existing caches, if any.  
      More areas within the cache can be populated than actually requested.

The provided region must be constructed to include the scale with which the image source will subsequently be drawn.  
      These coordinates must be provided in local coordinates.  
      This means that they must be adjusted prior to calling the API according to the DPI and other relevant transforms, 
      which can include the world transform and brush transforms.

This operation is only supported when the image source has been initialized using the D2D1_IMAGE_SOURCE_LOADING_OPTIONS_CACHE_ON_DEMAND option.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic">ID2D1ImageSourceFromWic</a>
