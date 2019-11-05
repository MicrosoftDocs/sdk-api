---
UID: NF:d2d1_1.ID2D1Properties.SetValue(U,const BYTE,UINT32)
title: ID2D1Properties::SetValue(U,const BYTE,UINT32,) (d2d1_1.h)
author: windows-sdk-content
description: Sets the corresponding property by index. This is a template overload.
old-location: direct2d\id2d1properties_setvalue3.htm
tech.root: Direct2D
ms.assetid: F0351C64-03CC-42D5-9622-F92C1054632C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1Properties interface [Direct2D],SetValue method, ID2D1Properties.SetValue, ID2D1Properties.SetValue(U,const BYTE,UINT32,), ID2D1Properties::SetValue, ID2D1Properties::SetValue(U,const BYTE*,UINT32), ID2D1Properties::SetValue(U,const BYTE,UINT32,), SetValue, SetValue method [Direct2D], SetValue method [Direct2D],ID2D1Properties interface, d2d1_1/ID2D1Properties::SetValue, direct2d.id2d1properties_setvalue3
ms.topic: method
f1_keywords: 
 - "d2d1_1/ID2D1Properties.SetValue"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Properties.SetValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Properties::SetValue(U,const BYTE,UINT32)


## -description


Sets the corresponding  property by index. This is a template overload. See Remarks.


## -parameters




### -param index

The index of the property to set.


### -param data [in]

The data to set.


### -param dataSize

The number of bytes in the data to set.


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
 




## -remarks




<pre class="syntax">template&lt;typename U&gt;
    HRESULT SetValue(
        U index,
        _In_reads_(dataSize) CONST BYTE *data,
        UINT32 dataSize
        );
</pre>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property">D2D1_PROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_subproperty">D2D1_SUBPROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>
 

 

