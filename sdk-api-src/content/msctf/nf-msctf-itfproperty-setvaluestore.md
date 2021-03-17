---
UID: NF:msctf.ITfProperty.SetValueStore
title: ITfProperty::SetValueStore (msctf.h)
description: ITfProperty::SetValueStore method
helpviewer_keywords: ["ITfProperty interface [Text Services Framework]","SetValueStore method","ITfProperty.SetValueStore","ITfProperty::SetValueStore","SetValueStore","SetValueStore method [Text Services Framework]","SetValueStore method [Text Services Framework]","ITfProperty interface","_tsf_itfproperty_setvaluestore_ref","msctf/ITfProperty::SetValueStore","tsf.itfproperty_setvaluestore"]
old-location: tsf\itfproperty_setvaluestore.htm
tech.root: TSF
ms.assetid: 146af429-54a8-41b6-b44e-b5d35f933435
ms.date: 12/05/2018
ms.keywords: ITfProperty interface [Text Services Framework],SetValueStore method, ITfProperty.SetValueStore, ITfProperty::SetValueStore, SetValueStore, SetValueStore method [Text Services Framework], SetValueStore method [Text Services Framework],ITfProperty interface, _tsf_itfproperty_setvaluestore_ref, msctf/ITfProperty::SetValueStore, tsf.itfproperty_setvaluestore
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
 - ITfProperty::SetValueStore
 - msctf/ITfProperty::SetValueStore
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
 - ITfProperty.SetValueStore
---

# ITfProperty::SetValueStore


## -description

Sets the value of the property for a range of text using a property store object.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that contains the range that the property value is set for. This parameter cannot be <b>NULL</b>. This method fails if <i>pRange</i> is empty.

### -param pPropStore [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfpropertystore">ITfPropertyStore</a> interface that obtains the property data.

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
</table>

## -remarks

Property values set with <a href="/windows/desktop/api/msctf/nf-msctf-itfproperty-setvalue">ITfProperty::SetValue</a> will be discarded when the text that the property value covers is modified. To gain control over what happens to a property value when the text is modified, use <b>ITfProperty::SetValueStore</b> .

Values set with <b>ITfProperty::SetValue</b> will be serialized, except for values of type VT_UNKNOWN, which are not serialized. If a property value of type VT_UNKNOWN must be serialized, use <b>ITfProperty::SetValueStore</b> instead.

Overlapping property values of the same type are unsupported.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfproperty">ITfProperty</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfproperty-setvalue">ITfProperty::SetValue
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfpropertystore">ITfPropertyStore
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>