---
UID: NN:d2d1.ID2D1Image
title: ID2D1Image (d2d1.h)
description: Represents a producer of pixels that can fill an arbitrary 2D plane. (ID2D1Image)
helpviewer_keywords: ["ID2D1Image","ID2D1Image interface [Direct2D]","ID2D1Image interface [Direct2D]","described","d2d1/ID2D1Image","direct2d.id2d1image"]
old-location: direct2d\id2d1image.htm
tech.root: Direct2D
ms.assetid: 9f7b4546-edbe-4000-a4ce-1a69563ebf9d
ms.date: 12/05/2018
ms.keywords: ID2D1Image, ID2D1Image interface [Direct2D], ID2D1Image interface [Direct2D],described, d2d1/ID2D1Image, direct2d.id2d1image
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Image
 - d2d1/ID2D1Image
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Image
---

# ID2D1Image interface


## -description

Represents a producer of pixels that can fill an arbitrary 2D plane.

## -remarks

An <b>ID2D1Image</b> is abstract.  Concrete instances can be created through <a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a> and <a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1)">ID2D1DeviceContext::CreateBitmap</a>.

Images are evaluated lazily. If the type of image passed in is concrete, then the image can be directly sampled from. Other images can act only as a source of pixels and can produce content only as a result of calling <a href="/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a>.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>



<a href="/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>



<a href="/windows/win32/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a>

