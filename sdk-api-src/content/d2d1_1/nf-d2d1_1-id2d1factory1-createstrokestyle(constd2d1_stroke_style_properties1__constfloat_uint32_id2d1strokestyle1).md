---
UID: NF:d2d1_1.ID2D1Factory1.CreateStrokeStyle(constD2D1_STROKE_STYLE_PROPERTIES1&,constFLOAT,UINT32,ID2D1StrokeStyle1)
title: ID2D1Factory1::CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &,const FLOAT,UINT32,ID2D1StrokeStyle1) (d2d1_1.h)
description: Creates a ID2D1StrokeStyle1 object. (overload 1/2)
helpviewer_keywords: ["CreateStrokeStyle","CreateStrokeStyle method [Direct2D]","CreateStrokeStyle method [Direct2D]","ID2D1Factory1 interface","ID2D1Factory1 interface [Direct2D]","CreateStrokeStyle method","ID2D1Factory1.CreateStrokeStyle","ID2D1Factory1.CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &","const FLOAT","UINT32","ID2D1StrokeStyle1)","ID2D1Factory1::CreateStrokeStyle","ID2D1Factory1::CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &","const FLOAT","UINT32","ID2D1StrokeStyle1)","d2d1_1/ID2D1Factory1::CreateStrokeStyle","direct2d.id2d1factory1_createstrokestyle2"]
old-location: direct2d\id2d1factory1_createstrokestyle2.htm
tech.root: Direct2D
ms.assetid: 4DEB9CDE-ABE2-47CB-BB06-27535F89D793
ms.date: 12/05/2018
ms.keywords: CreateStrokeStyle, CreateStrokeStyle method [Direct2D], CreateStrokeStyle method [Direct2D],ID2D1Factory1 interface, ID2D1Factory1 interface [Direct2D],CreateStrokeStyle method, ID2D1Factory1.CreateStrokeStyle, ID2D1Factory1.CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &,const FLOAT,UINT32,ID2D1StrokeStyle1), ID2D1Factory1::CreateStrokeStyle, ID2D1Factory1::CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &,const FLOAT,UINT32,ID2D1StrokeStyle1), d2d1_1/ID2D1Factory1::CreateStrokeStyle, direct2d.id2d1factory1_createstrokestyle2
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory1::CreateStrokeStyle
 - d2d1_1/ID2D1Factory1::CreateStrokeStyle
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
 - ID2D1Factory1.CreateStrokeStyle
---

# ID2D1Factory1::CreateStrokeStyle(const D2D1_STROKE_STYLE_PROPERTIES1 &,const FLOAT,UINT32,ID2D1StrokeStyle1)


## -description

Creates a <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1">ID2D1StrokeStyle1</a> object.

## -parameters

### -param strokeStyleProperties [in, ref]

Type: <b>const <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_stroke_style_properties1">D2D1_STROKE_STYLE_PROPERTIES1</a></b>

The stroke style properties to apply.

### -param dashes [in]

Type: <b>const <a href="/windows/desktop/api/wingdi/ns-wingdi-abcfloat">FLOAT</a>*</b>

An array of widths for the dashes and gaps.

### -param dashesCount

Type: <b><a href="/windows/desktop/api/webservices/ns-webservices-ws_uint64_description">UINT</a></b>

The size of the dash array.

### -param strokeStyle [out]

Type: <b>const <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1">ID2D1StrokeStyle1</a>**</b>

When this method returns, contains the address of a pointer to the  newly created stroke style.

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

It is valid to specify a dash array only if D2D1_DASH_STYLE_CUSTOM is also specified.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1">ID2D1Factory1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1">ID2D1StrokeStyle1</a>
