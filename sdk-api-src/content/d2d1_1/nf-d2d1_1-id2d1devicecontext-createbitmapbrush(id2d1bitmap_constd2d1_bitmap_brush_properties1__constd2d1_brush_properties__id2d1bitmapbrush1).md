---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateBitmapBrush(ID2D1Bitmap,constD2D1_BITMAP_BRUSH_PROPERTIES1&,constD2D1_BRUSH_PROPERTIES&,ID2D1BitmapBrush1)
title: ID2D1DeviceContext::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES1 &,const D2D1_BRUSH_PROPERTIES &,ID2D1BitmapBrush1) (d2d1_1.h)
description: Creates a bitmap brush, the input image is a Direct2D bitmap object. (overload 4/4)
helpviewer_keywords: ["CreateBitmapBrush","CreateBitmapBrush method [Direct2D]","CreateBitmapBrush method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","CreateBitmapBrush method","ID2D1DeviceContext.CreateBitmapBrush","ID2D1DeviceContext.CreateBitmapBrush(ID2D1Bitmap","const D2D1_BITMAP_BRUSH_PROPERTIES1 &","const D2D1_BRUSH_PROPERTIES &","ID2D1BitmapBrush1)","ID2D1DeviceContext::CreateBitmapBrush","ID2D1DeviceContext::CreateBitmapBrush(ID2D1Bitmap","const D2D1_BITMAP_BRUSH_PROPERTIES1 &","const D2D1_BRUSH_PROPERTIES &","ID2D1BitmapBrush1)","d2d1_1/ID2D1DeviceContext::CreateBitmapBrush","direct2d.id2d1devicecontext_createbitmapbrush"]
old-location: direct2d\id2d1devicecontext_createbitmapbrush.htm
tech.root: Direct2D
ms.assetid: E6385DBD-1A3B-4504-9987-35258E90DBC7
ms.date: 12/05/2018
ms.keywords: CreateBitmapBrush, CreateBitmapBrush method [Direct2D], CreateBitmapBrush method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateBitmapBrush method, ID2D1DeviceContext.CreateBitmapBrush, ID2D1DeviceContext.CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES1 &,const D2D1_BRUSH_PROPERTIES &,ID2D1BitmapBrush1), ID2D1DeviceContext::CreateBitmapBrush, ID2D1DeviceContext::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES1 &,const D2D1_BRUSH_PROPERTIES &,ID2D1BitmapBrush1), d2d1_1/ID2D1DeviceContext::CreateBitmapBrush, direct2d.id2d1devicecontext_createbitmapbrush
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
 - ID2D1DeviceContext::CreateBitmapBrush
 - d2d1_1/ID2D1DeviceContext::CreateBitmapBrush
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
 - ID2D1DeviceContext.CreateBitmapBrush
---

# ID2D1DeviceContext::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES1 &,const D2D1_BRUSH_PROPERTIES &,ID2D1BitmapBrush1)


## -description

Creates a bitmap brush, the input image is a Direct2D bitmap object.

## -parameters

### -param bitmap [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap to use as the brush.

### -param bitmapBrushProperties [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1">D2D1_BITMAP_BRUSH_PROPERTIES1</a>*</b>

A bitmap brush properties structure.

### -param brushProperties [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties">D2D1_BRUSH_PROPERTIES</a>*</b>

A brush properties structure.

### -param bitmapBrush [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1">ID2D1BitmapBrush1</a>**</b>

The address of the newly created bitmap brush object.

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

## -see-also

<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1">D2D1_BITMAP_BRUSH_PROPERTIES1</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap)">D2D1_BRUSH_PROPERTIES</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1">ID2D1BitmapBrush1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>
