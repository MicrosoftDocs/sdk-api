---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap,ID2D1BitmapBrush)
title: ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,ID2D1BitmapBrush)
author: windows-sdk-content
description: Creates an ID2D1BitmapBrush from the specified bitmap. The brush uses the default values for its extend mode, interpolation mode, opacity, and transform.
old-location: direct2d\ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ptr_ptr_ID2D1BitmapBrush.htm
tech.root: direct2d
ms.assetid: 6db7db16-ab2f-466b-8b57-bd0e0aef8691
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CreateBitmapBrush, CreateBitmapBrush method [Direct2D], CreateBitmapBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapBrush method, ID2D1RenderTarget.CreateBitmapBrush, ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap,ID2D1BitmapBrush), ID2D1RenderTarget::CreateBitmapBrush, ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,ID2D1BitmapBrush), d2d1/ID2D1RenderTarget::CreateBitmapBrush, direct2d.ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ptr_ptr_ID2D1BitmapBrush
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID2D1RenderTarget.CreateBitmapBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,ID2D1BitmapBrush)


## -description


Creates an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> from the specified bitmap. The brush uses the default values for its extend mode, interpolation mode, opacity, and transform.


## -parameters




### -param bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The bitmap contents of the new brush.


### -param bitmapBrush [out]

Type: <b><a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>**</b>

When this method returns, contains a pointer to a pointer to the new brush. This parameter is passed uninitialized.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The bitmap brush created by this method has <a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE_CLAMP</a>  horizontal and vertical extend modes and the <a href="https://msdn.microsoft.com/b53b7e0a-aa8b-4788-896c-9825c9e6cceb">D2D1_BITMAP_INTERPOLATION_MODE_LINEAR</a> interpolation mode. Its opacity is 1.0f, and its transform is the identity matrix.


#### Examples

For an example showing how to paint an area with a bitmap brush, see <a href="https://msdn.microsoft.com/8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d">How to Create a Bitmap Brush</a>. 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d">How to Create a Bitmap Brush</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

