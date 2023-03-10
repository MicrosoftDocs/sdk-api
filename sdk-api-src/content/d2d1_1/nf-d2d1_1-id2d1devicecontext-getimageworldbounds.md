---
UID: NF:d2d1_1.ID2D1DeviceContext.GetImageWorldBounds
title: ID2D1DeviceContext::GetImageWorldBounds (d2d1_1.h)
description: Gets the bounds of an image with the world transform of the context applied.
helpviewer_keywords: ["GetImageWorldBounds","GetImageWorldBounds method [Direct2D]","GetImageWorldBounds method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","GetImageWorldBounds method","ID2D1DeviceContext.GetImageWorldBounds","ID2D1DeviceContext::GetImageWorldBounds","d2d1_1/ID2D1DeviceContext::GetImageWorldBounds","direct2d.id2d1devicecontext_getimageworldbounds"]
old-location: direct2d\id2d1devicecontext_getimageworldbounds.htm
tech.root: Direct2D
ms.assetid: 939531E1-B641-48EF-B129-AC3AA5226919
ms.date: 12/05/2018
ms.keywords: GetImageWorldBounds, GetImageWorldBounds method [Direct2D], GetImageWorldBounds method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetImageWorldBounds method, ID2D1DeviceContext.GetImageWorldBounds, ID2D1DeviceContext::GetImageWorldBounds, d2d1_1/ID2D1DeviceContext::GetImageWorldBounds, direct2d.id2d1devicecontext_getimageworldbounds
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
 - ID2D1DeviceContext::GetImageWorldBounds
 - d2d1_1/ID2D1DeviceContext::GetImageWorldBounds
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
 - ID2D1DeviceContext.GetImageWorldBounds
---

# ID2D1DeviceContext::GetImageWorldBounds


## -description

Gets the bounds of an image with the world transform of the context applied.

## -parameters

### -param image [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>*</b>

The image whose bounds will be calculated.

### -param worldBounds [out]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>[1]</b>

When this method returns, contains a pointer to the bounds of the image in device independent pixels (DIPs).

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

The image bounds reflect the current DPI, unit mode, and world transform of the context.  To get bounds which don't include the world transform, use <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getimagelocalbounds">ID2D1DeviceContext::GetImageLocalBounds</a>.




The returned bounds reflect which pixels would be impacted by calling <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">DrawImage</a> with the same image and a target offset of (0,0).  They do not reflect the current clip rectangle set on the device context or the extent of the context’s current target image.

## -see-also

<a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1_id2d1bitmap1)">ID2D1DeviceContext::CreateBitmap</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-getimagelocalbounds">ID2D1DeviceContext::GetImageLocalBounds</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>