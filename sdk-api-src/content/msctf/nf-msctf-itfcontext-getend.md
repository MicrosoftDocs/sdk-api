---
UID: NF:msctf.ITfContext.GetEnd
title: ITfContext::GetEnd (msctf.h)
description: ITfContext::GetEnd method
helpviewer_keywords: ["GetEnd","GetEnd method [Text Services Framework]","GetEnd method [Text Services Framework]","ITfContext interface","ITfContext interface [Text Services Framework]","GetEnd method","ITfContext.GetEnd","ITfContext::GetEnd","_tsf_itfcontext_getend_ref","msctf/ITfContext::GetEnd","tsf.itfcontext_getend"]
old-location: tsf\itfcontext_getend.htm
tech.root: TSF
ms.assetid: 4fdae76d-ad02-43a4-8a39-418cae847ae8
ms.date: 12/05/2018
ms.keywords: GetEnd, GetEnd method [Text Services Framework], GetEnd method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],GetEnd method, ITfContext.GetEnd, ITfContext::GetEnd, _tsf_itfcontext_getend_ref, msctf/ITfContext::GetEnd, tsf.itfcontext_getend
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
 - ITfContext::GetEnd
 - msctf/ITfContext::GetEnd
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
 - ITfContext.GetEnd
---

# ITfContext::GetEnd


## -description

Obtains a range of text positioned at the end of the document.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit session. This is the value passed to <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param ppEnd [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface pointer that receives an empty range positioned at the end of the document.

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
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The cookie in <i>ec</i> is invalid.

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

## -see-also

[ITfContext interface](nn-msctf-itfcontext.md), [ITfEditSession::DoEditSession](nf-msctf-itfeditsession-doeditsession.md), [ITfRange interface](nn-msctf-itfrange.md)