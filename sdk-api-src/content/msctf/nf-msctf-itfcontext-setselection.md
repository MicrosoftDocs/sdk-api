---
UID: NF:msctf.ITfContext.SetSelection
title: ITfContext::SetSelection (msctf.h)
description: ITfContext::SetSelection method
helpviewer_keywords: ["ITfContext interface [Text Services Framework]","SetSelection method","ITfContext.SetSelection","ITfContext::SetSelection","SetSelection","SetSelection method [Text Services Framework]","SetSelection method [Text Services Framework]","ITfContext interface","_tsf_itfcontext_setselection_ref","msctf/ITfContext::SetSelection","tsf.itfcontext_setselection"]
old-location: tsf\itfcontext_setselection.htm
tech.root: TSF
ms.assetid: 1cf50b5e-6ec2-4649-9acc-743a2e3d8096
ms.date: 12/05/2018
ms.keywords: ITfContext interface [Text Services Framework],SetSelection method, ITfContext.SetSelection, ITfContext::SetSelection, SetSelection, SetSelection method [Text Services Framework], SetSelection method [Text Services Framework],ITfContext interface, _tsf_itfcontext_setselection_ref, msctf/ITfContext::SetSelection, tsf.itfcontext_setselection
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
 - ITfContext::SetSelection
 - msctf/ITfContext::SetSelection
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
 - ITfContext.SetSelection
---

# ITfContext::SetSelection


## -description

Sets the selection within the document.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit session. This is the value passed to <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param ulCount [in]

Specifies the number of selections in the <i>pSelection</i> array.

### -param pSelection [in]

An array of <a href="/windows/desktop/api/msctf/ns-msctf-tf_selection">TF_SELECTION</a> structures that contain the information for each selection.

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
</table>

## -remarks

A selection is a span of highlighted text, or an insertion point if the span is empty, identifying the user focus area within a document. Some documents are capable of having multiple selections. There can only be one zero-length selection in <i>pSelection</i> as it represents the position of the document caret.

If an application must adjust the text covered by a selection, it should wait until the caller releases the lock. However, applications can adjust any of the <b>style</b> members of the <b>TF_SELECTION</b> structures while still returning S_OK.

The caller can set the <b>fInterimChar</b> flag only if one selection is set. In this case, the selection should span exactly one character and the <b>ase</b> member of the <b>TF_SELECTION</b> structure is set to TFAE_NONE.

## -see-also

[ITfContext interface](nn-msctf-itfcontext.md), [ITfEditSession::DoEditSession](nf-msctf-itfeditsession-doeditsession.md), [TF_SELECTION structure](ns-msctf-tf_selection.md), [ITfContext::GetSelection](nf-msctf-itfcontext-getselection.md)