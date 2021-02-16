---
UID: NF:textstor.ITextStoreACP.SetSelection
title: ITextStoreACP::SetSelection (textstor.h)
description: The ITextStoreACP::SetSelection method selects text within the document. The application must have a read/write lock on the document before calling this method.
helpviewer_keywords: ["ITextStoreACP interface [Text Services Framework]","SetSelection method","ITextStoreACP.SetSelection","ITextStoreACP::SetSelection","SetSelection","SetSelection method [Text Services Framework]","SetSelection method [Text Services Framework]","ITextStoreACP interface","_tsf_itextstoreacp_setselection_ref","textstor/ITextStoreACP::SetSelection","tsf.itextstoreacp_setselection"]
old-location: tsf\itextstoreacp_setselection.htm
tech.root: TSF
ms.assetid: e9151b63-2ca7-4995-a36b-b919ab2d491a
ms.date: 12/05/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],SetSelection method, ITextStoreACP.SetSelection, ITextStoreACP::SetSelection, SetSelection, SetSelection method [Text Services Framework], SetSelection method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_setselection_ref, textstor/ITextStoreACP::SetSelection, tsf.itextstoreacp_setselection
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITextStoreACP::SetSelection
 - textstor/ITextStoreACP::SetSelection
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
 - ITextStoreACP.SetSelection
---

# ITextStoreACP::SetSelection


## -description

The <b>ITextStoreACP::SetSelection</b> method selects text within the document. The application must have a read/write lock on the document before calling this method.

## -parameters

### -param ulCount [in]

Specifies the number of text selections in <i>pSelection</i>.

### -param pSelection [in]

Specifies the style, start, and end character positions of the text selected through the <a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_acp">TS_SELECTION_ACP</a> structure.

When the start and end character positions are equal, the method places a caret at that character position. There can be only one caret at a time in the document.

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
<dt><b>TF_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The character positions specified are beyond the text in the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read/write lock.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getselection">ITextStoreACP::GetSelection
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_acp">TS_SELECTION_ACP
      </a>