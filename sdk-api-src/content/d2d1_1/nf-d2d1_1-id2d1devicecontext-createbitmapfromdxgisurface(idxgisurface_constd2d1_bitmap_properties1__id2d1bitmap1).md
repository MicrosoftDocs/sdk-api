---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateBitmapFromDxgiSurface(IDXGISurface,constD2D1_BITMAP_PROPERTIES1&,ID2D1Bitmap1)
title: ID2D1DeviceContext::CreateBitmapFromDxgiSurface(IDXGISurface,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1) (d2d1_1.h)
description: Creates a bitmap from a DXGI surface that can be set as a target surface or have additional color context information specified. (overload 2/2)
helpviewer_keywords: ["CreateBitmapFromDxgiSurface","CreateBitmapFromDxgiSurface method [Direct2D]","CreateBitmapFromDxgiSurface method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","CreateBitmapFromDxgiSurface method","ID2D1DeviceContext.CreateBitmapFromDxgiSurface","ID2D1DeviceContext.CreateBitmapFromDxgiSurface(IDXGISurface","const D2D1_BITMAP_PROPERTIES1 &","ID2D1Bitmap1)","ID2D1DeviceContext::CreateBitmapFromDxgiSurface","ID2D1DeviceContext::CreateBitmapFromDxgiSurface(IDXGISurface","const D2D1_BITMAP_PROPERTIES1 &","ID2D1Bitmap1)","d2d1_1/ID2D1DeviceContext::CreateBitmapFromDxgiSurface","direct2d.id2d1devicecontext_createbitmapfromdxgisurface"]
old-location: direct2d\id2d1devicecontext_createbitmapfromdxgisurface.htm
tech.root: Direct2D
ms.assetid: 76d49be7-b0ac-44a7-aeaf-a7b18346a2bf
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromDxgiSurface, CreateBitmapFromDxgiSurface method [Direct2D], CreateBitmapFromDxgiSurface method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateBitmapFromDxgiSurface method, ID2D1DeviceContext.CreateBitmapFromDxgiSurface, ID2D1DeviceContext.CreateBitmapFromDxgiSurface(IDXGISurface,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1), ID2D1DeviceContext::CreateBitmapFromDxgiSurface, ID2D1DeviceContext::CreateBitmapFromDxgiSurface(IDXGISurface,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1), d2d1_1/ID2D1DeviceContext::CreateBitmapFromDxgiSurface, direct2d.id2d1devicecontext_createbitmapfromdxgisurface
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
 - ID2D1DeviceContext::CreateBitmapFromDxgiSurface
 - d2d1_1/ID2D1DeviceContext::CreateBitmapFromDxgiSurface
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
 - ID2D1DeviceContext.CreateBitmapFromDxgiSurface
---

# ID2D1DeviceContext::CreateBitmapFromDxgiSurface(IDXGISurface,const D2D1_BITMAP_PROPERTIES1 &,ID2D1Bitmap1)


## -description

 Creates a bitmap from a DXGI surface that can be set as a target surface or have additional color context information specified.

## -parameters

### -param surface [in]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>*</b>

The DXGI surface from which the bitmap can be created.  

<div class="alert"><b>Note</b>  The DXGI surface must have been created from the same Direct3D device that the Direct2D device context is associated with.
</div>
<div> </div>

### -param bitmapProperties [in, optional]

Type: <b>const <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a>*</b>

The bitmap properties specified in addition to the surface.

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

If the bitmap properties are not specified, the following information is assumed: 

<ul>
<li>The bitmap DPI is 96.</li>
<li>The pixel format matches that of the surface.</li>
<li>The returned bitmap will inherit the bind flags of the DXGI surface.<ul>
<li>However, only the subset of flags meaningful to Direct2D will be inherited. For example, D3D10_USAGE_DYNAMIC is not compatible with any public Direct2D flags.</li>
</ul>
</li>
<li>The color context is unknown.</li>
<li>The alpha mode of the bitmap will be premultiplied (common case) or straight (A8).
</li>
</ul>
If the bitmap properties are specified, the bitmap properties will be used as follows:

<ul>
<li>The bitmap DPI will be specified by the bitmap properties.</li>
<li>If both dpiX and dpiY are 0, the bitmap DPI will be 96.</li>
<li>The pixel format must be compatible with the shader resource view or render target view of the surface.</li>
<li>The bitmap options must be compatible with the bind flags of the DXGI surface. However, they may be a subset. This will influence what resource views are created by the bitmap.</li>
<li>The color context information will be used from the bitmap properties, if specified.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget">ID2D1DeviceContext::SetTarget</a>
