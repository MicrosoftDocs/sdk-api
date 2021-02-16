---
UID: NF:d2d1_1.ID2D1Bitmap1.GetSurface
title: ID2D1Bitmap1::GetSurface (d2d1_1.h)
description: Gets either the surface that was specified when the bitmap was created, or the default surface created when the bitmap was created.
helpviewer_keywords: ["GetSurface","GetSurface method [Direct2D]","GetSurface method [Direct2D]","ID2D1Bitmap1 interface","ID2D1Bitmap1 interface [Direct2D]","GetSurface method","ID2D1Bitmap1.GetSurface","ID2D1Bitmap1::GetSurface","d2d1_1/ID2D1Bitmap1::GetSurface","direct2d.id2d1bitmap1_getsurface"]
old-location: direct2d\id2d1bitmap1_getsurface.htm
tech.root: Direct2D
ms.assetid: f9cb3830-7c1a-4254-a3fd-f1c056bec0c0
ms.date: 12/05/2018
ms.keywords: GetSurface, GetSurface method [Direct2D], GetSurface method [Direct2D],ID2D1Bitmap1 interface, ID2D1Bitmap1 interface [Direct2D],GetSurface method, ID2D1Bitmap1.GetSurface, ID2D1Bitmap1::GetSurface, d2d1_1/ID2D1Bitmap1::GetSurface, direct2d.id2d1bitmap1_getsurface
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
 - ID2D1Bitmap1::GetSurface
 - d2d1_1/ID2D1Bitmap1::GetSurface
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
 - ID2D1Bitmap1.GetSurface
---

# ID2D1Bitmap1::GetSurface


## -description

Gets either the surface that was specified when the bitmap was created, or the default surface created when the bitmap was created.

## -parameters

### -param dxgiSurface [out, optional]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>**</b>

The underlying DXGI surface for the bitmap.

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
<td>D2DERR_BITMAP_BOUND_AS_TARGET</td>
<td>Cannot draw with a bitmap that is currently bound as the target bitmap.</td>
</tr>
</table>

## -remarks

The bitmap used must have been created from a DXGI surface render target, a derived render target, or a device context created from an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>.

The returned surface can be used with Microsoft Direct3D or any other API that interoperates with shared surfaces. The application must transitively ensure that the surface is usable on the Direct3D device that is used in this context. For example, if using the surface with Direct2D  then the Direct2D render target must have been created through <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties_id2d1rendertarget)">ID2D1Factory::CreateDxgiSurfaceRenderTarget</a> or on a device context created on the same device.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1)">ID2D1DeviceContext::CreateBitmap</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)">ID2D1DeviceContext::CreateBitmapFromDxgiSurface</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap">ID2D1RenderTarget::CreateSharedBitmap</a>