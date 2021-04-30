---
UID: NF:qnetwork.IAMMediaContent.get_Copyright
title: IAMMediaContent::get_Copyright (qnetwork.h)
description: The get_Copyright method retrieves copyright information.
helpviewer_keywords: ["IAMMediaContent interface [DirectShow]","get_Copyright method","IAMMediaContent.get_Copyright","IAMMediaContent::get_Copyright","IAMMediaContentget_Copyright","dshow.iammediacontent_get_copyright","get_Copyright","get_Copyright method [DirectShow]","get_Copyright method [DirectShow]","IAMMediaContent interface","qnetwork/IAMMediaContent::get_Copyright"]
old-location: dshow\iammediacontent_get_copyright.htm
tech.root: dshow
ms.assetid: f63dc869-6b95-4923-80a6-22b5d8b81fa0
ms.date: 12/05/2018
ms.keywords: IAMMediaContent interface [DirectShow],get_Copyright method, IAMMediaContent.get_Copyright, IAMMediaContent::get_Copyright, IAMMediaContentget_Copyright, dshow.iammediacontent_get_copyright, get_Copyright, get_Copyright method [DirectShow], get_Copyright method [DirectShow],IAMMediaContent interface, qnetwork/IAMMediaContent::get_Copyright
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaContent::get_Copyright
 - qnetwork/IAMMediaContent::get_Copyright
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMMediaContent.get_Copyright
---

# IAMMediaContent::get_Copyright


## -description

The <code>get_Copyright</code> method retrieves copyright information.

## -parameters

### -param pbstrCopyright

Pointer to a variable that receives a <b>BSTR</b> with the information.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Item not found.

</td>
</tr>
</table>

## -remarks

If the method succeeds, the caller must free the returned <b>BSTR</b> by calling the <b>SysFreeString</b> function.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iammediacontent">IAMMediaContent Interface</a>