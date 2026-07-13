---
UID: NF:d2d1_1.ID2D1Properties.SetValueByName(PCWSTR,D2D1_PROPERTY_TYPE,constBYTE,UINT32)
title: ID2D1Properties::SetValueByName (d2d1_1.h)
description: Sets the named property to the given value. (overload 2/2)
helpviewer_keywords: ["ID2D1Properties interface [Direct2D]","SetValueByName method","ID2D1Properties.SetValueByName","ID2D1Properties::SetValueByName","ID2D1Properties::SetValueByName(PCWSTR","const BYTE*","UINT32)","ID2D1Properties::SetValueByName(PCWSTR","const BYTE","UINT32)","SetValueByName","SetValueByName method [Direct2D]","SetValueByName method [Direct2D]","ID2D1Properties interface","d2d1_1/ID2D1Properties::SetValueByName","direct2d.id2d1properties_setvaluebyname"]
old-location: direct2d\id2d1properties_setvaluebyname.htm
tech.root: Direct2D
ms.assetid: 3faedf5e-9329-4502-a1c9-162fd7b00319
ms.date: 12/05/2018
ms.keywords: ID2D1Properties interface [Direct2D],SetValueByName method, ID2D1Properties.SetValueByName, ID2D1Properties::SetValueByName, ID2D1Properties::SetValueByName(PCWSTR,const BYTE*,UINT32), ID2D1Properties::SetValueByName(PCWSTR,const BYTE,UINT32), SetValueByName, SetValueByName method [Direct2D], SetValueByName method [Direct2D],ID2D1Properties interface, d2d1_1/ID2D1Properties::SetValueByName, direct2d.id2d1properties_setvaluebyname
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
 - ID2D1Properties::SetValueByName
 - d2d1_1/ID2D1Properties::SetValueByName
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
 - ID2D1Properties.SetValueByName
---

# ID2D1Properties::SetValueByName


## -description

Sets the named property to the given value.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

The name of the property to set.

### -param type

TBD

### -param data [in]

Type: <b>const BYTE*</b>

The data to set.

### -param dataSize

Type: <b>UINT32</b>

The number of bytes in the data to set.

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

## -remarks

If the property does not exist, the request is ignored and the method returns <b>D2DERR_INVALID_PROPERTY</b>.

Any error not in the standard set returned by a property implementation will be mapped into the standard error range.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>
