---
UID: NF:textstor.ITextStoreACPSink.OnAttrsChange
title: ITextStoreACPSink::OnAttrsChange (textstor.h)
description: ITextStoreACPSink::OnAttrsChange method
helpviewer_keywords: ["ITextStoreACPSink interface [Text Services Framework]","OnAttrsChange method","ITextStoreACPSink.OnAttrsChange","ITextStoreACPSink::OnAttrsChange","OnAttrsChange","OnAttrsChange method [Text Services Framework]","OnAttrsChange method [Text Services Framework]","ITextStoreACPSink interface","_tsf_itextstoreacpsink_onattrschange_ref","textstor/ITextStoreACPSink::OnAttrsChange","tsf.itextstoreacpsink_onattrschange"]
old-location: tsf\itextstoreacpsink_onattrschange.htm
tech.root: TSF
ms.assetid: ae1e5f92-7462-46b4-b4dd-5032147de688
ms.date: 12/05/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnAttrsChange method, ITextStoreACPSink.OnAttrsChange, ITextStoreACPSink::OnAttrsChange, OnAttrsChange, OnAttrsChange method [Text Services Framework], OnAttrsChange method [Text Services Framework],ITextStoreACPSink interface, _tsf_itextstoreacpsink_onattrschange_ref, textstor/ITextStoreACPSink::OnAttrsChange, tsf.itextstoreacpsink_onattrschange
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
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
 - ITextStoreACPSink::OnAttrsChange
 - textstor/ITextStoreACPSink::OnAttrsChange
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
 - ITextStoreACPSink.OnAttrsChange
---

# ITextStoreACPSink::OnAttrsChange


## -description

Called when the value of one or more text attribute changes.

## -parameters

### -param acpStart [in]

Specifies the starting point of the attribute change.

### -param acpEnd [in]

Specifies the ending point of the attribute change.

### -param cAttrs [in]

Specifies the number of attributes in the <i>paAttrs</i> array.

### -param paAttrs [in]

Pointer to an array of <a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID</a> values that identify the attributes changed.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>