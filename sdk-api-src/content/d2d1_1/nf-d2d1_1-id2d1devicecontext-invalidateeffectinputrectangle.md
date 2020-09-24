---
UID: NF:d2d1_1.ID2D1DeviceContext.InvalidateEffectInputRectangle
title: ID2D1DeviceContext::InvalidateEffectInputRectangle (d2d1_1.h)
description: This indicates that a portion of an effect's input is invalid. This method can be called many times.
helpviewer_keywords: ["ID2D1DeviceContext interface [Direct2D]","InvalidateEffectInputRectangle method","ID2D1DeviceContext.InvalidateEffectInputRectangle","ID2D1DeviceContext::InvalidateEffectInputRectangle","InvalidateEffectInputRectangle","InvalidateEffectInputRectangle method [Direct2D]","InvalidateEffectInputRectangle method [Direct2D]","ID2D1DeviceContext interface","d2d1_1/ID2D1DeviceContext::InvalidateEffectInputRectangle","direct2d.id2d1devicecontext_invalidateeffectinputrectangle"]
old-location: direct2d\id2d1devicecontext_invalidateeffectinputrectangle.htm
tech.root: Direct2D
ms.assetid: 3EB22E7B-69B4-4936-B8ED-093EA1EA1759
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],InvalidateEffectInputRectangle method, ID2D1DeviceContext.InvalidateEffectInputRectangle, ID2D1DeviceContext::InvalidateEffectInputRectangle, InvalidateEffectInputRectangle, InvalidateEffectInputRectangle method [Direct2D], InvalidateEffectInputRectangle method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::InvalidateEffectInputRectangle, direct2d.id2d1devicecontext_invalidateeffectinputrectangle
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
 - ID2D1DeviceContext::InvalidateEffectInputRectangle
 - d2d1_1/ID2D1DeviceContext::InvalidateEffectInputRectangle
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
 - ID2D1DeviceContext.InvalidateEffectInputRectangle
---

# ID2D1DeviceContext::InvalidateEffectInputRectangle


## -description

This indicates that a portion of an effect's input is invalid. This method can
     be called many times.

You can use this method to propagate invalid rectangles through an effect graph. You can query Direct2D using the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-geteffectinvalidrectangles">GetEffectInvalidRectangles</a> method.
<div class="alert"><b>Note</b>  Direct2D does not automatically use these invalid rectangles to reduce the region of an effect that is rendered.</div><div> </div>You can also use this method to invalidate caches that have accumulated while rendering effects that have the <b>D2D1_PROPERTY_CACHED</b> property set to true.

## -parameters

### -param effect [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>*</b>

The effect to invalidate.

### -param input

Type: <b>UINT32</b>

The input index.

### -param inputRectangle [in]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The rect to invalidate.

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

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>