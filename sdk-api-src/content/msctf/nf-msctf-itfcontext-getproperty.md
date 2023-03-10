---
UID: NF:msctf.ITfContext.GetProperty
title: ITfContext::GetProperty (msctf.h)
description: ITfContext::GetProperty method
helpviewer_keywords: ["GetProperty","GetProperty method [Text Services Framework]","GetProperty method [Text Services Framework]","ITfContext interface","ITfContext interface [Text Services Framework]","GetProperty method","ITfContext.GetProperty","ITfContext::GetProperty","_tsf_itfcontext_getproperty_ref","msctf/ITfContext::GetProperty","tsf.itfcontext_getproperty"]
old-location: tsf\itfcontext_getproperty.htm
tech.root: TSF
ms.assetid: e5d76443-f767-47fb-be3a-8cbac224d299
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Text Services Framework], GetProperty method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],GetProperty method, ITfContext.GetProperty, ITfContext::GetProperty, _tsf_itfcontext_getproperty_ref, msctf/ITfContext::GetProperty, tsf.itfcontext_getproperty
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContext::GetProperty
 - msctf/ITfContext::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContext.GetProperty
---

# ITfContext::GetProperty


## -description

Obtains a text property.

## -parameters

### -param guidProp [in]

Specifies the property identifier. This can be a custom identifier or one of the <a href="/windows/desktop/TSF/predefined-properties">predefined property identifiers</a>.

### -param ppProp [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfproperty">ITfProperty</a> interface pointer that receives the property object.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

An application or text service can define unique properties identified by a GUID. Properties are stored as VARIANT data, so the caller must recognize the format and meaning of unique properties to be able to use them.

## -see-also

[ITfContext interface](nn-msctf-itfcontext.md), [ITfProperty interface](nn-msctf-itfproperty.md), [Predefined Properties](/windows/desktop/TSF/predefined-properties)