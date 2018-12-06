---
UID: NN:d2d1.ID2D1BitmapBrush
title: ID2D1BitmapBrush
author: windows-sdk-content
description: Paints an area with a bitmap.
old-location: direct2d\ID2D1BitmapBrush.htm
tech.root: direct2d
ms.assetid: 22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1BitmapBrush, ID2D1BitmapBrush interface [Direct2D], ID2D1BitmapBrush interface [Direct2D],described, d2d1/ID2D1BitmapBrush, direct2d.ID2D1BitmapBrush
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1BitmapBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1BitmapBrush interface


## -description


Paints an area with a bitmap.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1BitmapBrush</b> interface inherits from <a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>. <b>ID2D1BitmapBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1BitmapBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/754eb1d7-bce6-42bd-9b51-9565e31f1d73">GetBitmap</a>
</td>
<td align="left" width="63%">
Gets the bitmap source that this brush uses to paint.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/167c5aff-b070-4020-87c4-1385e014f22a">GetExtendModeX</a>
</td>
<td align="left" width="63%">
  Gets the method by which the brush horizontally tiles those areas that extend past its bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e71fef61-9d6a-441b-a88f-9f2cead23ecd">GetExtendModeY</a>
</td>
<td align="left" width="63%">
  Gets the method by which the brush vertically tiles those areas that extend past its bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0bc487b-3259-4f25-b4ab-7468ccf96d98">GetInterpolationMode</a>
</td>
<td align="left" width="63%">
Gets the interpolation method used when the brush bitmap is scaled or rotated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/776dba7f-11d0-4055-9071-8719ac192f00">SetBitmap</a>
</td>
<td align="left" width="63%">
Specifies the bitmap source that this brush uses to paint. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb20c9ea-a2b1-4fa5-a0e3-b788fe493993">SetExtendModeX</a>
</td>
<td align="left" width="63%">
Specifies how the brush horizontally tiles those areas that extend past its bitmap. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6039ad41-e4b4-41e2-a4b1-31ad93ba88fd">SetExtendModeY</a>
</td>
<td align="left" width="63%">
Specifies how the brush vertically tiles those areas that extend past its bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad2a4211-c8ae-4242-9d6a-6548375f52a7">SetInterpolationMode</a>
</td>
<td align="left" width="63%">
Specifies the interpolation mode used when the brush bitmap is scaled or rotated.

</td>
</tr>
</table> 


## -remarks



A bitmap brush is used to fill a geometry with a bitmap. Like all brushes, it defines an infinite plane of content. Because bitmaps are finite, the brush relies on an "extend mode" to determine how the plane is filled horizontally and vertically.

<h3><a id="Creating_ID2D1BitmapBrush_Objects"></a><a id="creating_id2d1bitmapbrush_objects"></a><a id="CREATING_ID2D1BITMAPBRUSH_OBJECTS"></a>Creating ID2D1BitmapBrush Objects</h3>
To create a bitmap brush, use the <a href="https://msdn.microsoft.com/7f6ef07e-4271-4605-aced-f191a0fe65af">ID2D1RenderTarget::CreateBitmapBrush</a> method.

An <b>ID2D1BitmapBrush</b> is a device-dependent resource: your application should create bitmap brushes after it initializes the render target with which the bitmap brush will be used, and recreate the bitmap brush whenever the render target needs recreated. (For more information about resources, see <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.)


#### Examples

For an example of how to create a bitmap brush, see the <a href="https://msdn.microsoft.com/8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d">How to Create a Bitmap Brush</a> topic. 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d">How to Create a Bitmap Brush</a>



<a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>



<a href="https://msdn.microsoft.com/869821b0-6ebe-46c2-aab6-93177d8a92c5">Opacity Masks Overview</a>
 

 

