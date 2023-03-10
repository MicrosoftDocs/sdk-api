---
UID: NF:msctf.ITfContext.GetSelection
title: ITfContext::GetSelection (msctf.h)
description: ITfContext::GetSelection method
helpviewer_keywords: ["GetSelection","GetSelection method [Text Services Framework]","GetSelection method [Text Services Framework]","ITfContext interface","ITfContext interface [Text Services Framework]","GetSelection method","ITfContext.GetSelection","ITfContext::GetSelection","_tsf_itfcontext_getselection_ref","msctf/ITfContext::GetSelection","tsf.itfcontext_getselection"]
old-location: tsf\itfcontext_getselection.htm
tech.root: TSF
ms.assetid: 08b67fd5-aebe-49f7-af78-6f49c8f47f64
ms.date: 12/05/2018
ms.keywords: GetSelection, GetSelection method [Text Services Framework], GetSelection method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],GetSelection method, ITfContext.GetSelection, ITfContext::GetSelection, _tsf_itfcontext_getselection_ref, msctf/ITfContext::GetSelection, tsf.itfcontext_getselection
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
 - ITfContext::GetSelection
 - msctf/ITfContext::GetSelection
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
 - ITfContext.GetSelection
---

# ITfContext::GetSelection


## -description

Obtains the selection within the document.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit session. This is the value passed to <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param ulIndex [in]

Specifies the zero-based index of the first selection to obtain. Use TF_DEFAULT_SELECTION to obtain the default selection. If TF_DEFAULT_SELECTION is used, only one selection is obtained.

### -param ulCount [in]

Specifies the maximum number of selections to obtain.

### -param pSelection [out]

An array of <a href="/windows/desktop/api/msctf/ns-msctf-tf_selection">TF_SELECTION</a> structures that receives the data for each selection. The array must be able to hold at least <i>ulCount</i> elements.

### -param pcFetched [out]

Pointer to a ULONG value that receives the number of selections obtained.

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
<dt><b>TF_E_NOSELECTION</b></dt>
</dl>
</td>
<td width="60%">
The document has no selection.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

A selection is a highlighted range of text, or an insertion point if the range is empty, that identifies the user focus area within a document.

If this method is successful, the caller must release the <b>range</b> member of all <b>TF_SELECTION</b> structures obtained.

Normally, a context only supports a single selection. It is possible, however, for a context to support multiple, simultaneous selections. This method can be used to obtain multiple selections.

## Examples

```cpp

HRESULT         hr;
TF_SELECTION    tfSel;
ULONG           uFetched;

//Obtain the default selection. 
hr = pContext->GetSelection(ec, TF_DEFAULT_SELECTION, 1, &tfSel, &uFetched);
if(SUCCEEDED(hr) && (uFetched > 0))
{
    //Work with the selection. 
    
    //Release the selection range object. 
    tfSel.range->Release();
}

```

## -see-also

[ITfContext interface](nn-msctf-itfcontext.md), [ITfEditSession::DoEditSession](nf-msctf-itfeditsession-doeditsession.md), [TF_SELECTION structure](ns-msctf-tf_selection.md), [ITfContext::SetSelection](nf-msctf-itfcontext-setselection.md)