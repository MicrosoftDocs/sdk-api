---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateBorderTransform
title: ID2D1EffectContext::CreateBorderTransform (d2d1effectauthor.h)
description: Creates a transform that extends its input infinitely in every direction based on the passed in extend mode.
helpviewer_keywords: ["CreateBorderTransform","CreateBorderTransform method [Direct2D]","CreateBorderTransform method [Direct2D]","ID2D1EffectContext interface","ID2D1EffectContext interface [Direct2D]","CreateBorderTransform method","ID2D1EffectContext.CreateBorderTransform","ID2D1EffectContext::CreateBorderTransform","d2d1effectauthor/ID2D1EffectContext::CreateBorderTransform","direct2d.id2d1contextinternal_createbordertransform"]
old-location: direct2d\id2d1contextinternal_createbordertransform.htm
tech.root: Direct2D
ms.assetid: E1FC2BF9-7287-4F9B-BDCF-3CD6EC8B849D
ms.date: 12/05/2018
ms.keywords: CreateBorderTransform, CreateBorderTransform method [Direct2D], CreateBorderTransform method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateBorderTransform method, ID2D1EffectContext.CreateBorderTransform, ID2D1EffectContext::CreateBorderTransform, d2d1effectauthor/ID2D1EffectContext::CreateBorderTransform, direct2d.id2d1contextinternal_createbordertransform
req.header: d2d1effectauthor.h
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
req.lib: D2D1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectContext::CreateBorderTransform
 - d2d1effectauthor/ID2D1EffectContext::CreateBorderTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext.CreateBorderTransform
---

# ID2D1EffectContext::CreateBorderTransform


## -description

Creates a transform that extends its input infinitely in every direction based on the passed in extend mode.

## -parameters

### -param extendModeX

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

The extend mode in the X-axis direction.

### -param extendModeY

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE</a></b>

The extend mode in the Y-axis direction.

### -param transform [out]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform">ID2D1BorderTransform</a>**</b>

The returned transform.

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

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext">ID2D1EffectContext</a>