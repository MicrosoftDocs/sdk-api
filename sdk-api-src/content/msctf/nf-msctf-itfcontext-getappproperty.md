---
UID: NF:msctf.ITfContext.GetAppProperty
title: ITfContext::GetAppProperty (msctf.h)
description: ITfContext::GetAppProperty method
helpviewer_keywords: ["GetAppProperty","GetAppProperty method [Text Services Framework]","GetAppProperty method [Text Services Framework]","ITfContext interface","ITfContext interface [Text Services Framework]","GetAppProperty method","ITfContext.GetAppProperty","ITfContext::GetAppProperty","_tsf_itfcontext_getappproperty_ref","msctf/ITfContext::GetAppProperty","tsf.itfcontext_getappproperty"]
old-location: tsf\itfcontext_getappproperty.htm
tech.root: TSF
ms.assetid: 5c04ff8e-5686-4802-b312-71dddaf0155e
ms.date: 12/05/2018
ms.keywords: GetAppProperty, GetAppProperty method [Text Services Framework], GetAppProperty method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],GetAppProperty method, ITfContext.GetAppProperty, ITfContext::GetAppProperty, _tsf_itfcontext_getappproperty_ref, msctf/ITfContext::GetAppProperty, tsf.itfcontext_getappproperty
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
 - ITfContext::GetAppProperty
 - msctf/ITfContext::GetAppProperty
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
 - ITfContext.GetAppProperty
---

# ITfContext::GetAppProperty


## -description

Obtains an application property.

## -parameters

### -param guidProp [in]

Specifies the property identifier. This can be a custom identifier or one of the <a href="/windows/desktop/TSF/predefined-properties">predefined property identifiers</a>.

### -param ppProp [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty">ITfReadOnlyProperty</a> interface pointer that receives the property object.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The context owner does not support the property.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The context owner does not implement this method.

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

Applications can define unique properties identified by a GUID. Properties are stored as VARIANT data, so the caller must recognize the format and meaning of unique properties to be able to use them.

Application properties differ from text properties, obtained by <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty">ITfContext::GetProperty</a>, in that, application properties are maintained by the context owner and cannot be modified by a text service. Application properties can only be modified by the context owner.

## -see-also

[ITfContext interface](nn-msctf-itfcontext.md), [ITfContext::GetProperty](nf-msctf-itfcontext-getproperty.md), [ITfReadOnlyProperty interface](nn-msctf-itfreadonlyproperty.md), [Predefined Properties](/windows/desktop/TSF/predefined-properties)