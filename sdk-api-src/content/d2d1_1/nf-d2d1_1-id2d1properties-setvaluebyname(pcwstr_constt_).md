---
UID: NF:d2d1_1.ID2D1Properties.SetValueByName(PCWSTR,constT&)
title: ID2D1Properties::SetValueByName(PCWSTR,const T &,) (d2d1_1.h)
description: Sets the named property to the given value. This is a template overload. See Remarks.
helpviewer_keywords: ["ID2D1Properties interface [Direct2D]","SetValueByName method","ID2D1Properties.SetValueByName","ID2D1Properties.SetValueByName(PCWSTR","const T &",")","ID2D1Properties::SetValueByName","ID2D1Properties::SetValueByName(PCWSTR","const T &",")","ID2D1Properties::SetValueByName(PCWSTR","const T&)","SetValueByName","SetValueByName method [Direct2D]","SetValueByName method [Direct2D]","ID2D1Properties interface","d2d1_1/ID2D1Properties::SetValueByName","direct2d.id2d1properties_setvaluebyname__pcwstr__const_t_"]
old-location: direct2d\id2d1properties_setvaluebyname__pcwstr__const_t_.htm
tech.root: Direct2D
ms.assetid: 50AC6CAF-16D6-4E10-8B9D-A91D5869D7E1
ms.date: 12/05/2018
ms.keywords: ID2D1Properties interface [Direct2D],SetValueByName method, ID2D1Properties.SetValueByName, ID2D1Properties.SetValueByName(PCWSTR,const T &,), ID2D1Properties::SetValueByName, ID2D1Properties::SetValueByName(PCWSTR,const T &,), ID2D1Properties::SetValueByName(PCWSTR,const T&), SetValueByName, SetValueByName method [Direct2D], SetValueByName method [Direct2D],ID2D1Properties interface, d2d1_1/ID2D1Properties::SetValueByName, direct2d.id2d1properties_setvaluebyname__pcwstr__const_t_
f1_keywords:
- d2d1_1/ID2D1Properties.SetValueByName
dev_langs:
- c++
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows�8 and Platform Update for Windows�7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server�2012 and Platform Update for Windows Server�2008�R2 [desktop apps \| UWP apps]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1Properties.SetValueByName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Properties::SetValueByName(PCWSTR,const T &)


## -description


Sets the named property to the given value.  This is a template overload. See Remarks.


## -parameters




### -param propertyName [in]

The name of the property to set.


### -param value [in, ref]

The data to set.  The method will convert this type to a BYTE* before setting it as the property value.


## -returns



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
�




## -remarks




<pre class="syntax">template&lt;typename T&gt;
    HRESULT SetValueByName(
        _In_ PCWSTR propertyName,
        _In_ const T &amp;value
        );
</pre>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>
�

�

