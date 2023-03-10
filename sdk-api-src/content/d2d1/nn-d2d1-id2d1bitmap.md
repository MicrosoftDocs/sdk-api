---
UID: NN:d2d1.ID2D1Bitmap
title: ID2D1Bitmap (d2d1.h)
description: Represents a bitmap that has been bound to an ID2D1RenderTarget.
helpviewer_keywords: ["ID2D1Bitmap","ID2D1Bitmap interface [Direct2D]","ID2D1Bitmap interface [Direct2D]","described","d2d1/ID2D1Bitmap","direct2d.ID2D1Bitmap"]
old-location: direct2d\ID2D1Bitmap.htm
tech.root: Direct2D
ms.assetid: e58216ea-e6b5-450f-a0ea-b879aa5dff38
ms.date: 12/05/2018
ms.keywords: ID2D1Bitmap, ID2D1Bitmap interface [Direct2D], ID2D1Bitmap interface [Direct2D],described, d2d1/ID2D1Bitmap, direct2d.ID2D1Bitmap
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Bitmap
 - d2d1/ID2D1Bitmap
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
 - ID2D1Bitmap
---

# ID2D1Bitmap interface


## -description

Represents a bitmap that has been bound to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>.

## -inheritance

The <b>ID2D1Bitmap</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>. <b>ID2D1Bitmap</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

<h3><a id="Creating_ID2D1Bitmap_Objects"></a><a id="creating_id2d1bitmap_objects"></a><a id="CREATING_ID2D1BITMAP_OBJECTS"></a>Creating ID2D1Bitmap Objects</h3>
To create a bitmap, use one of the following methods of the render target on which the bitmap will be drawn: <ul>
<li>
<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constd2d1_bitmap_properties__id2d1bitmap)">ID2D1RenderTarget::CreateBitmap</a>
</li>
<li>
<a href="/windows/win32/Direct2D/id2d1rendertarget-createbitmapfromwicbitmap">ID2D1RenderTarget::CreateBitmapFromWicBitmap</a>
</li>
</ul>


For information about the pixel formats supported by Direct2D bitmaps, see <a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>.

An <b>ID2D1Bitmap</b> is a device-dependent resource: your application should create bitmaps after it initializes the render target with which the bitmap will be used, and recreate the bitmap whenever the render target needs recreated. (For more information about resources, see <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.)


## Examples

For examples that show how to create an <b>ID2D1Bitmap</b> from a WIC bitmap, see <a href="/windows/win32/Direct2D/how-to-load-a-direct2d-bitmap-from-a-file">How to Load a   Bitmap from a File</a> and <a href="/windows/win32/Direct2D/how-to-load-a-bitmap-from-a-resource">How to Load a Bitmap from a Resource</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/Direct2D/how-to-load-a-direct2d-bitmap-from-a-file">How to Load a   Bitmap from a File</a>



<a href="/windows/win32/Direct2D/how-to-load-a-bitmap-from-a-resource">How to Load a Bitmap from a Resource</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>



<a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>

