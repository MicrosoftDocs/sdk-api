---
UID: NF:d2d1_1.ID2D1DeviceContext.GetEffectInvalidRectangleCount
title: ID2D1DeviceContext::GetEffectInvalidRectangleCount (d2d1_1.h)
description: Gets the number of invalid output rectangles that have accumulated on the effect.
helpviewer_keywords: ["GetEffectInvalidRectangleCount","GetEffectInvalidRectangleCount method [Direct2D]","GetEffectInvalidRectangleCount method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","GetEffectInvalidRectangleCount method","ID2D1DeviceContext.GetEffectInvalidRectangleCount","ID2D1DeviceContext::GetEffectInvalidRectangleCount","d2d1_1/ID2D1DeviceContext::GetEffectInvalidRectangleCount","direct2d.id2d1devicecontext_geteffectinvalidrectanglecount"]
old-location: direct2d\id2d1devicecontext_geteffectinvalidrectanglecount.htm
tech.root: Direct2D
ms.assetid: C0B70DA1-C9BF-47AC-BF3E-2A741DACD2E8
ms.date: 12/05/2018
ms.keywords: GetEffectInvalidRectangleCount, GetEffectInvalidRectangleCount method [Direct2D], GetEffectInvalidRectangleCount method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetEffectInvalidRectangleCount method, ID2D1DeviceContext.GetEffectInvalidRectangleCount, ID2D1DeviceContext::GetEffectInvalidRectangleCount, d2d1_1/ID2D1DeviceContext::GetEffectInvalidRectangleCount, direct2d.id2d1devicecontext_geteffectinvalidrectanglecount
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
 - ID2D1DeviceContext::GetEffectInvalidRectangleCount
 - d2d1_1/ID2D1DeviceContext::GetEffectInvalidRectangleCount
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
 - ID2D1DeviceContext.GetEffectInvalidRectangleCount
---

# ID2D1DeviceContext::GetEffectInvalidRectangleCount


## -description

Gets the number of invalid output rectangles that have accumulated on the effect.

## -parameters

### -param effect [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>*</b>

The effect to count the invalid rectangles on.

### -param rectangleCount [out]

Type: <b>UINT32*</b>

The returned rectangle count.

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