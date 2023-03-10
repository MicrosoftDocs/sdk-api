---
UID: NN:d2d1_1.ID2D1Bitmap1
title: ID2D1Bitmap1 (d2d1_1.h)
description: Represents a bitmap that can be used as a surface for an ID2D1DeviceContext or mapped into system memory, and can contain additional color context information.
helpviewer_keywords: ["ID2D1Bitmap1","ID2D1Bitmap1 interface [Direct2D]","ID2D1Bitmap1 interface [Direct2D]","described","d2d1_1/ID2D1Bitmap1","direct2d.id2d1bitmap1"]
old-location: direct2d\id2d1bitmap1.htm
tech.root: Direct2D
ms.assetid: 669a9377-248c-4a86-b447-ed117fff43a6
ms.date: 12/05/2018
ms.keywords: ID2D1Bitmap1, ID2D1Bitmap1 interface [Direct2D], ID2D1Bitmap1 interface [Direct2D],described, d2d1_1/ID2D1Bitmap1, direct2d.id2d1bitmap1
req.header: d2d1_1.h
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
 - ID2D1Bitmap1
 - d2d1_1/ID2D1Bitmap1
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
 - ID2D1Bitmap1
---

# ID2D1Bitmap1 interface


## -description

Represents a bitmap that can be used as a surface for an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a> or mapped into system memory, and can contain additional color context information.

## -inheritance

The <b>ID2D1Bitmap1</b> interface inherits from <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>. <b>ID2D1Bitmap1</b> also has these types of members:

## -remarks

<h3><a id="Creating_ID2D1Bitmap_Objects"></a><a id="creating_id2d1bitmap_objects"></a><a id="CREATING_ID2D1BITMAP_OBJECTS"></a>Creating ID2D1Bitmap Objects</h3>
Use one of these methods to create an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a> object. <ul>
<li>
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1)">ID2D1DeviceContext::CreateBitmap</a>
</li>
<li>
<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1)">ID2D1DeviceContext::CreateBitmapFromWicBitmap</a>
</li>
</ul>


For information about the pixel formats supported by Direct2D bitmaps, see <a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>.

An <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a> is a device-dependent resource: your application should create bitmaps after it initializes the render target with which the bitmap will be used, and recreate the bitmap whenever the render target needs recreated. (For more information about resources, see <a href="/windows/desktop/Direct2D/resources-and-resource-domains">Resources Overview</a>.)

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>
