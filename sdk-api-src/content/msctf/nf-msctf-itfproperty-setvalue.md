---
UID: NF:msctf.ITfProperty.SetValue
title: ITfProperty::SetValue (msctf.h)
description: ITfProperty::SetValue method
helpviewer_keywords: ["ITfProperty interface [Text Services Framework]","SetValue method","ITfProperty.SetValue","ITfProperty::SetValue","SetValue","SetValue method [Text Services Framework]","SetValue method [Text Services Framework]","ITfProperty interface","_tsf_itfproperty_setvalue_ref","msctf/ITfProperty::SetValue","tsf.itfproperty_setvalue"]
old-location: tsf\itfproperty_setvalue.htm
tech.root: TSF
ms.assetid: 72064f9f-311e-4d7b-9ead-4fe2b7f528a8
ms.date: 12/05/2018
ms.keywords: ITfProperty interface [Text Services Framework],SetValue method, ITfProperty.SetValue, ITfProperty::SetValue, SetValue, SetValue method [Text Services Framework], SetValue method [Text Services Framework],ITfProperty interface, _tsf_itfproperty_setvalue_ref, msctf/ITfProperty::SetValue, tsf.itfproperty_setvalue
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
 - ITfProperty::SetValue
 - msctf/ITfProperty::SetValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfProperty.SetValue
---

# ITfProperty::SetValue


## -description

Sets the value of the property for a range.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that contains the range that the property value is set for. This parameter cannot be <b>NULL</b>. This method will fail if <i>pRange</i> is empty.

### -param pvarValue [in]

Pointer to a <b>VARIANT</b> structure that contains the new property value. Only values of type VT_I4, VT_UNKNOWN, VT_BSTR and VT_EMPTY are supported.

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
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ec</i> does not have a read/write lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
The edit context is read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOTOWNEDRANGE</b></dt>
</dl>
</td>
<td width="60%">
The TSF manager does not own the range.

</td>
</tr>
</table>

## -remarks

Property values set with this method will be discarded when the text that the property value covers is modified. To gain custom control over a value response to text edits, use <a href="/windows/desktop/api/msctf/nf-msctf-itfproperty-setvaluestore">ITfProperty::SetValueStore</a>.

Values set with this method are serialized, except for values of type VT_UNKNOWN, which are not serialized. If a property value of type VT_UNKNOWN must be serialized, use <b>ITfProperty::SetValueStore</b> instead.

Overlapping property values of the same type are unsupported.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfproperty">ITfProperty</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfproperty-setvaluestore">ITfProperty::SetValueStore
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>