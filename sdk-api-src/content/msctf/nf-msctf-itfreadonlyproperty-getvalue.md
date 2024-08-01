---
UID: NF:msctf.ITfReadOnlyProperty.GetValue
title: ITfReadOnlyProperty::GetValue (msctf.h)
description: ITfReadOnlyProperty::GetValue method
helpviewer_keywords: ["GetValue","GetValue method [Text Services Framework]","GetValue method [Text Services Framework]","ITfReadOnlyProperty interface","ITfReadOnlyProperty interface [Text Services Framework]","GetValue method","ITfReadOnlyProperty.GetValue","ITfReadOnlyProperty::GetValue","_tsf_itfreadonlyproperty_getvalue_ref","msctf/ITfReadOnlyProperty::GetValue","tsf.itfreadonlyproperty_getvalue"]
old-location: tsf\itfreadonlyproperty_getvalue.htm
tech.root: TSF
ms.assetid: c82ef360-e0b1-4e1a-b839-36b8e9c52347
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Text Services Framework], GetValue method [Text Services Framework],ITfReadOnlyProperty interface, ITfReadOnlyProperty interface [Text Services Framework],GetValue method, ITfReadOnlyProperty.GetValue, ITfReadOnlyProperty::GetValue, _tsf_itfreadonlyproperty_getvalue_ref, msctf/ITfReadOnlyProperty::GetValue, tsf.itfreadonlyproperty_getvalue
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
 - ITfReadOnlyProperty::GetValue
 - msctf/ITfReadOnlyProperty::GetValue
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
 - ITfReadOnlyProperty.GetValue
---

# ITfReadOnlyProperty::GetValue


## -description

Obtains the value of the property for a range of text.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that specifies the range to obtain the property for.

### -param pvarValue [out]

Pointer to a <b>VARIANT</b> value that receives the property value. The data type and contents of this value is defined by the property owner and must be recognized by the caller in order to use this value. The caller must release this data, when it is no longer required, by passing this value to the <b>VariantClear</b> API.

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
The range is not covered by the property or the range contains more than one property value. <i>pvarValue</i> receives a VT_EMPTY value.

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
The edit context identified by <i>ec</i> does not have a read-only or read/write lock.

</td>
</tr>
</table>

## -remarks

If the property has no value over <i>pRange</i>, <i>pRange</i> contains more than one value for the property or the property does not completely cover <i>pRange</i>, <i>pvarValue</i> receives a VT_EMPTY value and the method returns S_FALSE.


``` syntax

COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
    range-->||<-

```


``` syntax

COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
    range-->|    |<-

```


``` syntax

COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
    range-->|             |<-

```


## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty">ITfReadOnlyProperty</a>
