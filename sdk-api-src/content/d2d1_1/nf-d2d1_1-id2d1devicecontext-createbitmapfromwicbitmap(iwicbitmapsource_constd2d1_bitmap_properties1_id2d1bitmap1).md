---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateBitmapFromWicBitmap(IWICBitmapSource,constD2D1_BITMAP_PROPERTIES1,ID2D1Bitmap1)
title: ID2D1DeviceContext::CreateBitmapFromWicBitmap (d2d1_1.h)
description: Creates a Direct2D bitmap by copying a WIC bitmap. (overload 2/2)
helpviewer_keywords: ["CreateBitmapFromWicBitmap","CreateBitmapFromWicBitmap method [Direct2D]","CreateBitmapFromWicBitmap method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","CreateBitmapFromWicBitmap method","ID2D1DeviceContext.CreateBitmapFromWicBitmap","ID2D1DeviceContext::CreateBitmapFromWicBitmap","ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource","const D2D1_BITMAP_PROPERTIES1","ID2D1Bitmap1)","d2d1_1/ID2D1DeviceContext::CreateBitmapFromWicBitmap","direct2d.id2d1devicecontext_createbitmapfromwicbitmap"]
old-location: direct2d\id2d1devicecontext_createbitmapfromwicbitmap.htm
tech.root: Direct2D
ms.assetid: 98BA78CD-4902-43B9-A412-895CA2A112C7
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromWicBitmap, CreateBitmapFromWicBitmap method [Direct2D], CreateBitmapFromWicBitmap method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateBitmapFromWicBitmap method, ID2D1DeviceContext.CreateBitmapFromWicBitmap, ID2D1DeviceContext::CreateBitmapFromWicBitmap, ID2D1DeviceContext::CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES1,ID2D1Bitmap1), d2d1_1/ID2D1DeviceContext::CreateBitmapFromWicBitmap, direct2d.id2d1devicecontext_createbitmapfromwicbitmap
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
 - ID2D1DeviceContext::CreateBitmapFromWicBitmap
 - d2d1_1/ID2D1DeviceContext::CreateBitmapFromWicBitmap
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
 - ID2D1DeviceContext.CreateBitmapFromWicBitmap
---

# ID2D1DeviceContext::CreateBitmapFromWicBitmap


## -description

Creates a Direct2D bitmap by copying a WIC bitmap.

## -parameters

### -param wicBitmapSource [in]

Type: <b>IWICBitmapSource*</b>

The WIC bitmap source to copy from.

### -param bitmapProperties [in, optional]

Type: <b>const <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1)">D2D1_BITMAP_PROPERTIES1</a>*</b>

A bitmap properties structure that specifies bitmap creation options.

### -param bitmap [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>**</b>

The address of the newly created bitmap object.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>

## -remarks

Starting with Windows 8.1, the  <i>bitmapProperties</i> parameter is optional. When it is not specified, the created bitmap inherits the pixel format and alpha mode from  <i>wicBitmapSource</i>. For a list of supported pixel formats and alpha modes, see <a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>.

When the <i>bitmapProperties</i> parameter is specified, the value in <i>bitmapProperties-&gt;pixelFormat</i> must either be <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_UNKNOWN</a> or must match the WIC pixel format in <i>wicBitmapSource</i>.

When <i>bitmapProperties-&gt;pixelFormat.alphaMode</i> is set to <a href="/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_UNKNOWN</a>, the newly created bitmap inherits the alpha mode from <i>wicBitmapSource</i>. When <i>bitmapProperties-&gt;pixelFormat.alphaMode</i> is set to <b>D2D1_ALPHA_MODE_PREMULTIPLIED</b>, <b>D2D1_ALPHA_MODE_STRAIGHT</b>, or <b>D2D1_ALPHA_MODE_IGNORE</b>, this forces the newly created bitmap to use the specified alpha mode.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>
