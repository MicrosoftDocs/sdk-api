---
UID: NN:d2d1.ID2D1Bitmap
title: ID2D1Bitmap (d2d1.h)
author: windows-sdk-content
description: Represents a bitmap that has been bound to an ID2D1RenderTarget.
old-location: direct2d\ID2D1Bitmap.htm
tech.root: Direct2D
ms.assetid: e58216ea-e6b5-450f-a0ea-b879aa5dff38
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1Bitmap, ID2D1Bitmap interface [Direct2D], ID2D1Bitmap interface [Direct2D],described, d2d1/ID2D1Bitmap, direct2d.ID2D1Bitmap
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
 - ID2D1Bitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Bitmap interface


## -description


Represents a bitmap that has been bound to an <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Bitmap</b> interface inherits from <a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>. <b>ID2D1Bitmap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Bitmap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d43685d9-292c-462c-bdd2-c4e81b6d704e">CopyFromBitmap</a>
</td>
<td align="left" width="63%">
Copies the specified region from the specified bitmap into the current bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/594cba56-6f18-439a-ada4-0f591af094bb">CopyFromMemory</a>
</td>
<td align="left" width="63%">
Copies the specified region from memory into the current bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42e25099-016e-4656-a412-72dd0fbac1fd">CopyFromRenderTarget</a>
</td>
<td align="left" width="63%">
Copies the specified region from the specified render target into the current bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50659165-86e9-4143-af88-a68e422a74e0">GetDpi</a>
</td>
<td align="left" width="63%">
Return the dots per inch (DPI) of the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e94a0930-f681-47d0-8cee-bacf631ee6db">GetPixelFormat</a>
</td>
<td align="left" width="63%">
Retrieves the pixel format and alpha mode of the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d51408a-2648-4984-bbc0-9846d5161c77">GetPixelSize</a>
</td>
<td align="left" width="63%">
Returns the size, in device-dependent units (pixels), of the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ab1d67d-d7ee-41a0-a298-738b1520ff3b">GetSize</a>
</td>
<td align="left" width="63%">
Returns the size, in device-independent pixels (DIPs), of the bitmap.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Creating_ID2D1Bitmap_Objects"></a><a id="creating_id2d1bitmap_objects"></a><a id="CREATING_ID2D1BITMAP_OBJECTS"></a>Creating ID2D1Bitmap Objects</h3>
To create a bitmap, use one of the following methods of the render target on which the bitmap will be drawn: <ul>
<li>
<a href="https://msdn.microsoft.com/76e91383-6da7-47ae-9d5e-a83d78556b29">ID2D1RenderTarget::CreateBitmap</a>
</li>
<li>
<a href="https://msdn.microsoft.com/463fc2f9-8ec6-47e8-8d48-a9015616e656">ID2D1RenderTarget::CreateBitmapFromWicBitmap</a>
</li>
</ul>


For information about the pixel formats supported by Direct2D bitmaps, see <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>.

An <b>ID2D1Bitmap</b> is a device-dependent resource: your application should create bitmaps after it initializes the render target with which the bitmap will be used, and recreate the bitmap whenever the render target needs recreated. (For more information about resources, see <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.)


#### Examples

For examples that show how to create an <b>ID2D1Bitmap</b> from a WIC bitmap, see <a href="https://msdn.microsoft.com/4abfbc2b-2730-4d96-897e-1e2232383a72">How to Load a   Bitmap from a File</a> and <a href="https://msdn.microsoft.com/7285e6ea-ebc7-4693-8a77-99bff0b5d0d1">How to Load a Bitmap from a Resource</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4abfbc2b-2730-4d96-897e-1e2232383a72">How to Load a   Bitmap from a File</a>



<a href="https://msdn.microsoft.com/7285e6ea-ebc7-4693-8a77-99bff0b5d0d1">How to Load a Bitmap from a Resource</a>



<a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>



<a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>
 

 

