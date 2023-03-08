---
UID: NN:d2d1.ID2D1BitmapBrush
title: ID2D1BitmapBrush (d2d1.h)
description: Paints an area with a bitmap. (ID2D1BitmapBrush)
helpviewer_keywords: ["ID2D1BitmapBrush","ID2D1BitmapBrush interface [Direct2D]","ID2D1BitmapBrush interface [Direct2D]","described","d2d1/ID2D1BitmapBrush","direct2d.ID2D1BitmapBrush"]
old-location: direct2d\ID2D1BitmapBrush.htm
tech.root: Direct2D
ms.assetid: 22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4
ms.date: 12/05/2018
ms.keywords: ID2D1BitmapBrush, ID2D1BitmapBrush interface [Direct2D], ID2D1BitmapBrush interface [Direct2D],described, d2d1/ID2D1BitmapBrush, direct2d.ID2D1BitmapBrush
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
 - ID2D1BitmapBrush
 - d2d1/ID2D1BitmapBrush
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
 - ID2D1BitmapBrush
---

# ID2D1BitmapBrush interface


## -description

Paints an area with a bitmap.

## -inheritance

The <b>ID2D1BitmapBrush</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>. <b>ID2D1BitmapBrush</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

A bitmap brush is used to fill a geometry with a bitmap. Like all brushes, it defines an infinite plane of content. Because bitmaps are finite, the brush relies on an "extend mode" to determine how the plane is filled horizontally and vertically.

<h3><a id="Creating_ID2D1BitmapBrush_Objects"></a><a id="creating_id2d1bitmapbrush_objects"></a><a id="CREATING_ID2D1BITMAPBRUSH_OBJECTS"></a>Creating ID2D1BitmapBrush Objects</h3>
To create a bitmap brush, use the <a href="/windows/win32/Direct2D/id2d1rendertarget-createbitmapbrush">ID2D1RenderTarget::CreateBitmapBrush</a> method.

An <b>ID2D1BitmapBrush</b> is a device-dependent resource: your application should create bitmap brushes after it initializes the render target with which the bitmap brush will be used, and recreate the bitmap brush whenever the render target needs recreated. (For more information about resources, see <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.)


## Examples

For an example of how to create a bitmap brush, see the <a href="/windows/win32/Direct2D/how-to-create-a-bitmap-brush">How to Create a Bitmap Brush</a> topic. 

<div class="code"></div>

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="/windows/win32/Direct2D/how-to-create-a-bitmap-brush">How to Create a Bitmap Brush</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>



<a href="/windows/win32/Direct2D/opacity-masks-overview">Opacity Masks Overview</a>

