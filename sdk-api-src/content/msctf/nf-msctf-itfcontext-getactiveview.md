---
UID: NF:msctf.ITfContext.GetActiveView
title: ITfContext::GetActiveView (msctf.h)
description: ITfContext::GetActiveView method
helpviewer_keywords: ["GetActiveView","GetActiveView method [Text Services Framework]","GetActiveView method [Text Services Framework]","ITfContext interface","ITfContext interface [Text Services Framework]","GetActiveView method","ITfContext.GetActiveView","ITfContext::GetActiveView","_tsf_itfcontext_getactiveview_ref","msctf/ITfContext::GetActiveView","tsf.itfcontext_getactiveview"]
old-location: tsf\itfcontext_getactiveview.htm
tech.root: TSF
ms.assetid: 41f7eb74-bca2-4d53-8a70-0b872616fd1b
ms.date: 12/05/2018
ms.keywords: GetActiveView, GetActiveView method [Text Services Framework], GetActiveView method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],GetActiveView method, ITfContext.GetActiveView, ITfContext::GetActiveView, _tsf_itfcontext_getactiveview_ref, msctf/ITfContext::GetActiveView, tsf.itfcontext_getactiveview
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
 - ITfContext::GetActiveView
 - msctf/ITfContext::GetActiveView
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
 - ITfContext.GetActiveView
---

# ITfContext::GetActiveView


## -description

Obtains the active view for the context.

## -parameters

### -param ppView [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfcontextview">ITfContextView</a> interface pointer that receives a reference to the active view.

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

[ITfContext interface](nn-msctf-itfcontext.md), [ITfContextView interface](nn-msctf-itfcontextview.md)