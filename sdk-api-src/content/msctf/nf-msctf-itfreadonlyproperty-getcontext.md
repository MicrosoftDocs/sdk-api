---
UID: NF:msctf.ITfReadOnlyProperty.GetContext
title: ITfReadOnlyProperty::GetContext (msctf.h)
description: ITfReadOnlyProperty::GetContext method
helpviewer_keywords: ["GetContext","GetContext method [Text Services Framework]","GetContext method [Text Services Framework]","ITfReadOnlyProperty interface","ITfReadOnlyProperty interface [Text Services Framework]","GetContext method","ITfReadOnlyProperty.GetContext","ITfReadOnlyProperty::GetContext","_tsf_itfreadonlyproperty_getcontext_ref","msctf/ITfReadOnlyProperty::GetContext","tsf.itfreadonlyproperty_getcontext"]
old-location: tsf\itfreadonlyproperty_getcontext.htm
tech.root: TSF
ms.assetid: 2f6becd7-c4d0-45ed-8038-1f706d8e60c7
ms.date: 12/05/2018
ms.keywords: GetContext, GetContext method [Text Services Framework], GetContext method [Text Services Framework],ITfReadOnlyProperty interface, ITfReadOnlyProperty interface [Text Services Framework],GetContext method, ITfReadOnlyProperty.GetContext, ITfReadOnlyProperty::GetContext, _tsf_itfreadonlyproperty_getcontext_ref, msctf/ITfReadOnlyProperty::GetContext, tsf.itfreadonlyproperty_getcontext
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
 - ITfReadOnlyProperty::GetContext
 - msctf/ITfReadOnlyProperty::GetContext
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
 - ITfReadOnlyProperty.GetContext
---

# ITfReadOnlyProperty::GetContext


## -description

Obtains the context object for the property.

## -parameters

### -param ppContext [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface pointer that receives the context object. The caller must release this object when it is no longer required.

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
<i>ppContext</i> is invalid.

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

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty">ITfReadOnlyProperty</a>