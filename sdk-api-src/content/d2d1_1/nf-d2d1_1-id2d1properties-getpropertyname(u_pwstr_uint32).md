---
UID: NF:d2d1_1.ID2D1Properties.GetPropertyName(U,PWSTR,UINT32)
title: ID2D1Properties::GetPropertyName(U,PWSTR,UINT32,) (d2d1_1.h)
description: Gets the property name that corresponds to the given index. This is a template overload. See Remarks.
helpviewer_keywords: ["GetPropertyName","GetPropertyName method [Direct2D]","GetPropertyName method [Direct2D]","ID2D1Properties interface","ID2D1Properties interface [Direct2D]","GetPropertyName method","ID2D1Properties.GetPropertyName","ID2D1Properties.GetPropertyName(U","PWSTR","UINT32",")","ID2D1Properties::GetPropertyName","ID2D1Properties::GetPropertyName(U","PWSTR","UINT32)","ID2D1Properties::GetPropertyName(U","PWSTR","UINT32",")","d2d1_1/ID2D1Properties::GetPropertyName","direct2d.id2d1properties_getpropertyname2"]
old-location: direct2d\id2d1properties_getpropertyname2.htm
tech.root: Direct2D
ms.assetid: 777BF543-F2AF-4B17-BF2B-845D713EA5CA
ms.date: 12/05/2018
ms.keywords: GetPropertyName, GetPropertyName method [Direct2D], GetPropertyName method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetPropertyName method, ID2D1Properties.GetPropertyName, ID2D1Properties.GetPropertyName(U,PWSTR,UINT32,), ID2D1Properties::GetPropertyName, ID2D1Properties::GetPropertyName(U,PWSTR,UINT32), ID2D1Properties::GetPropertyName(U,PWSTR,UINT32,), d2d1_1/ID2D1Properties::GetPropertyName, direct2d.id2d1properties_getpropertyname2
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
 - ID2D1Properties::GetPropertyName
 - d2d1_1/ID2D1Properties::GetPropertyName
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
 - ID2D1Properties.GetPropertyName
---

# ID2D1Properties::GetPropertyName(U,PWSTR,UINT32)


## -description

Gets the property name that corresponds to the given index. This is a template overload. See Remarks.

## -parameters

### -param index

Type: <b>U</b>

The index of the property for which the name is being returned.

### -param name [out]

Type: <b>PWSTR</b>

When this method returns, contains the name being retrieved.

### -param nameCount

Type: <b>UINT32</b>

The number of characters in the <i>name</i> buffer.

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
<td>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</td>
<td>The supplied buffer was too small to accommodate the data.</td>
</tr>
<tr>
<td>D2DERR_INVALID_PROPERTY</td>
<td>The specified property does not exist.</td>
</tr>
</table>

## -remarks

This method returns an empty string if <i>index</i> is invalid. If the method returns <b>RESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b>, <i>name</i> will still be filled and truncated.


<pre class="syntax">template&lt;typename U&gt;
    HRESULT GetPropertyName(
        U index,
        _Out_writes_(nameCount) PWSTR name,
        UINT32 nameCount
        ) CONST;
</pre>

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property">D2D1_PROPERTY</a>



<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_subproperty">D2D1_SUBPROPERTY</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>
