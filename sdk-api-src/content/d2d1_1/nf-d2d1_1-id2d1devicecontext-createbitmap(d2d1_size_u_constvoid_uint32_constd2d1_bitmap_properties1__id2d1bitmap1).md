---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateBitmap(D2D1_SIZE_U,constvoid,UINT32,constD2D1_BITMAP_PROPERTIES1&,ID2D1Bitmap1)
title: ID2D1DeviceContext::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1) (d2d1_1.h)
description: Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the DrawBitmap and ID2D1BitmapBrush APIs. In addition, color context information can be passed to the bitmap. (overload 1/2)
helpviewer_keywords: ["CreateBitmap","CreateBitmap method [Direct2D]","CreateBitmap method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","CreateBitmap method","ID2D1DeviceContext.CreateBitmap","ID2D1DeviceContext.CreateBitmap(D2D1_SIZE_U","const void","UINT32","const D2D1_BITMAP_PROPERTIES1 &","ID2D1Bitmap1)","ID2D1DeviceContext::CreateBitmap","ID2D1DeviceContext::CreateBitmap(D2D1_SIZE_U","const void","UINT32","const D2D1_BITMAP_PROPERTIES1 &","ID2D1Bitmap1)","d2d1_1/ID2D1DeviceContext::CreateBitmap","direct2d.id2d1devicecontext_createbitmap"]
old-location: direct2d\id2d1devicecontext_createbitmap.htm
tech.root: Direct2D
ms.assetid: 8292da6b-8232-4ef0-967d-a53d586aa9a9
ms.date: 12/05/2018
ms.keywords: CreateBitmap, CreateBitmap method [Direct2D], CreateBitmap method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateBitmap method, ID2D1DeviceContext.CreateBitmap, ID2D1DeviceContext.CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1), ID2D1DeviceContext::CreateBitmap, ID2D1DeviceContext::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1), d2d1_1/ID2D1DeviceContext::CreateBitmap, direct2d.id2d1devicecontext_createbitmap
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
 - ID2D1DeviceContext::CreateBitmap
 - d2d1_1/ID2D1DeviceContext::CreateBitmap
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
 - ID2D1DeviceContext.CreateBitmap
---

# ID2D1DeviceContext::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1)


## -description

Creates a bitmap that can be used as a target surface, for reading back to the CPU, or as a source for the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_interpolation_mode_constd2d1_rect_f_constd2d1_matrix_4x4_f)">DrawBitmap</a> and <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> APIs. In addition, color context information can be passed to the bitmap.

## -parameters

### -param size

Type: <b><a href="/windows/desktop/Direct2D/d2d1-size-u">D2D1_SIZE_U</a></b>

The pixel size of the bitmap to be created.

### -param sourceData [in, optional]

Type: <b>const void*</b>

The initial data that will be loaded into the bitmap.

### -param pitch

Type: <b>UINT32</b>

The pitch of the source data, if specified.

### -param bitmapProperties [in]

Type: <b>const <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a>*</b>

The properties of the bitmap to be created.

### -param bitmap [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>**</b>

When this method returns, contains the address of a pointer to a new bitmap object.

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
<td>An invalid value was passed to the method.</td>
</tr>
<tr>
<td>D3DERR_OUTOFVIDEOMEMORY</td>
<td>Direct3D does not have enough display memory to perform the operation.</td>
</tr>
</table>

## -remarks

The new bitmap can be used as a target for <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget">SetTarget</a> if it is created with <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options">D2D1_BITMAP_OPTIONS_TARGET</a>.

## -see-also

<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a>



<a href="/windows/desktop/Direct2D/d2d1-size-u">D2D1_SIZE_U</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>
