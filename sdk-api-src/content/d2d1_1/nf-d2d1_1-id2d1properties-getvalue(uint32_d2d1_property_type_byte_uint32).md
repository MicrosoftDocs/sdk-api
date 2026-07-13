---
UID: NF:d2d1_1.ID2D1Properties.GetValue(UINT32,D2D1_PROPERTY_TYPE,BYTE,UINT32)
title: ID2D1Properties::GetValue (d2d1_1.h)
description: Gets the value of the specified property by index. (overload 2/2)
helpviewer_keywords: ["GetValue","GetValue method [Direct2D]","GetValue method [Direct2D]","ID2D1Properties interface","ID2D1Properties interface [Direct2D]","GetValue method","ID2D1Properties.GetValue","ID2D1Properties::GetValue","ID2D1Properties::GetValue(UINT32","BYTE*","UINT32)","ID2D1Properties::GetValue(UINT32","BYTE","UINT32)","d2d1_1/ID2D1Properties::GetValue","direct2d.id2d1properties_getvalue"]
old-location: direct2d\id2d1properties_getvalue.htm
tech.root: Direct2D
ms.assetid: 01678e13-df23-47bb-9af7-9f2ecaf03577
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Direct2D], GetValue method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetValue method, ID2D1Properties.GetValue, ID2D1Properties::GetValue, ID2D1Properties::GetValue(UINT32,BYTE*,UINT32), ID2D1Properties::GetValue(UINT32,BYTE,UINT32), d2d1_1/ID2D1Properties::GetValue, direct2d.id2d1properties_getvalue
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
 - ID2D1Properties::GetValue
 - d2d1_1/ID2D1Properties::GetValue
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
 - ID2D1Properties.GetValue
---

# ID2D1Properties::GetValue


## -description

Gets  the value of the specified property by index.

## -parameters

### -param index

Type: <b>UINT32</b>

The index of the property from which the data is to be obtained.

### -param type

TBD

### -param data [out]

Type: <b>BYTE*</b>

When this method returns, contains a pointer to the data requested.

### -param dataSize

Type: <b>UINT32</b>

The number of bytes in the data to be retrieved.

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
<td>D2DERR_INVALID_PROPERTY</td>
<td>The specified property does not exist.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Failed to allocate necessary memory.</td>
</tr>
<tr>
<td>D3DERR_OUT_OF_VIDEO_MEMORY</td>
<td>Failed to allocate required video memory.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>One or more arguments are invalid.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>Unspecified failure.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property">D2D1_PROPERTY</a>



<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_subproperty">D2D1_SUBPROPERTY</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>
