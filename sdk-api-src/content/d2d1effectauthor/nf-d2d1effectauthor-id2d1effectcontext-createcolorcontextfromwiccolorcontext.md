---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateColorContextFromWicColorContext
title: ID2D1EffectContext::CreateColorContextFromWicColorContext (d2d1effectauthor.h)
description: Creates a color context from an IWICColorContext. The D2D1ColorContext space of the resulting context varies, see Remarks for more info. (ID2D1EffectContext.CreateColorContextFromWicColorContext)
helpviewer_keywords: ["CreateColorContextFromWicColorContext","CreateColorContextFromWicColorContext method [Direct2D]","CreateColorContextFromWicColorContext method [Direct2D]","ID2D1EffectContext interface","ID2D1EffectContext interface [Direct2D]","CreateColorContextFromWicColorContext method","ID2D1EffectContext.CreateColorContextFromWicColorContext","ID2D1EffectContext::CreateColorContextFromWicColorContext","d2d1effectauthor/ID2D1EffectContext::CreateColorContextFromWicColorContext","direct2d.id2d1contextinternal_createcolorcontextfromwiccolorcontext"]
old-location: direct2d\id2d1contextinternal_createcolorcontextfromwiccolorcontext.htm
tech.root: Direct2D
ms.assetid: 4A269666-28A1-4A03-823B-60C6A1A9D73E
ms.date: 12/05/2018
ms.keywords: CreateColorContextFromWicColorContext, CreateColorContextFromWicColorContext method [Direct2D], CreateColorContextFromWicColorContext method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateColorContextFromWicColorContext method, ID2D1EffectContext.CreateColorContextFromWicColorContext, ID2D1EffectContext::CreateColorContextFromWicColorContext, d2d1effectauthor/ID2D1EffectContext::CreateColorContextFromWicColorContext, direct2d.id2d1contextinternal_createcolorcontextfromwiccolorcontext
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectContext::CreateColorContextFromWicColorContext
 - d2d1effectauthor/ID2D1EffectContext::CreateColorContextFromWicColorContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.dll
api_name:
 - ID2D1EffectContext.CreateColorContextFromWicColorContext
---

# ID2D1EffectContext::CreateColorContextFromWicColorContext


## -description

Creates a color context from an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>.  The <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">D2D1ColorContext</a> space of the resulting context varies, see Remarks for more info.

## -parameters

### -param wicColorContext [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>*</b>

The <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> used to initialize the color context.

### -param colorContext [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>**</b>

When this method returns, contains the address of a pointer to a new color context.

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
</table>

## -remarks

The new color context can be used in <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a> to initialize the color context of a created bitmap.  The model field of the profile header is inspected to determine whether this profile is sRGB or scRGB and the color space is updated respectively.  Otherwise the space is  custom.

## -see-also

<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext">ID2D1EffectContext</a>
