---
UID: NF:d2d1_1.ID2D1DeviceContext.GetEffectInvalidRectangles
title: ID2D1DeviceContext::GetEffectInvalidRectangles (d2d1_1.h)
description: Gets the invalid rectangles that have accumulated since the last time the effect was drawn and EndDraw was then called on the device context.
helpviewer_keywords: ["GetEffectInvalidRectangles","GetEffectInvalidRectangles method [Direct2D]","GetEffectInvalidRectangles method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","GetEffectInvalidRectangles method","ID2D1DeviceContext.GetEffectInvalidRectangles","ID2D1DeviceContext::GetEffectInvalidRectangles","d2d1_1/ID2D1DeviceContext::GetEffectInvalidRectangles","direct2d.id2d1devicecontext_geteffectinvalidrectangles"]
old-location: direct2d\id2d1devicecontext_geteffectinvalidrectangles.htm
tech.root: Direct2D
ms.assetid: D5CEFDB0-BD54-4CB9-801C-528CDA49C19C
ms.date: 12/05/2018
ms.keywords: GetEffectInvalidRectangles, GetEffectInvalidRectangles method [Direct2D], GetEffectInvalidRectangles method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetEffectInvalidRectangles method, ID2D1DeviceContext.GetEffectInvalidRectangles, ID2D1DeviceContext::GetEffectInvalidRectangles, d2d1_1/ID2D1DeviceContext::GetEffectInvalidRectangles, direct2d.id2d1devicecontext_geteffectinvalidrectangles
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
 - ID2D1DeviceContext::GetEffectInvalidRectangles
 - d2d1_1/ID2D1DeviceContext::GetEffectInvalidRectangles
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
 - ID2D1DeviceContext.GetEffectInvalidRectangles
---

# ID2D1DeviceContext::GetEffectInvalidRectangles


## -description

Gets the invalid rectangles that have accumulated since the last time the effect was drawn and <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> was then called on the device context.

## -parameters

### -param effect [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>*</b>

The effect to get the invalid rectangles from.

### -param rectangles [out]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

An array of <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a> structures.  You must allocate this to the correct size.  You can get the count of the invalid rectangles using the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-geteffectinvalidrectanglecount">GetEffectInvalidRectangleCount</a> method.

### -param rectanglesCount [in]

Type: <b>UINT32</b>

The number of rectangles to get.

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

<div class="alert"><b>Note</b>  Direct2D does not automatically use these invalid rectangles to reduce the region of an effect that is rendered.</div>
<div> </div>


You can use the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-invalidateeffectinputrectangle">InvalidateEffectInputRectangle</a> method to specify invalidated rectangles for Direct2D to propagate through an effect graph.

If multiple invalid rectangles are requested, the rectangles that this method returns may overlap. When this is the case, the rectangle count might be lower than the count that <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-geteffectinvalidrectanglecount">GetEffectInvalidRectangleCount</a>.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>