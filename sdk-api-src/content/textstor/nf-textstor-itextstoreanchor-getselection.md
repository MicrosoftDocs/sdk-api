---
UID: NF:textstor.ITextStoreAnchor.GetSelection
title: ITextStoreAnchor::GetSelection (textstor.h)
description: The ITextStoreAnchor::GetSelection method returns the offset of a text selection in a text stream. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.
helpviewer_keywords: ["GetSelection","GetSelection method [Text Services Framework]","GetSelection method [Text Services Framework]","ITextStoreAnchor interface","ITextStoreAnchor interface [Text Services Framework]","GetSelection method","ITextStoreAnchor.GetSelection","ITextStoreAnchor::GetSelection","textstor/ITextStoreAnchor::GetSelection","tsf.itextstoreanchor_getselection"]
old-location: tsf\itextstoreanchor_getselection.htm
tech.root: TSF
ms.assetid: df1b21b7-b539-4546-96be-243a8e7ea75a
ms.date: 12/05/2018
ms.keywords: GetSelection, GetSelection method [Text Services Framework], GetSelection method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetSelection method, ITextStoreAnchor.GetSelection, ITextStoreAnchor::GetSelection, textstor/ITextStoreAnchor::GetSelection, tsf.itextstoreanchor_getselection
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
 - ITextStoreAnchor::GetSelection
 - textstor/ITextStoreAnchor::GetSelection
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
 - ITextStoreAnchor.GetSelection
---

# ITextStoreAnchor::GetSelection


## -description

The <b>ITextStoreAnchor::GetSelection</b> method returns the offset of a text selection in a text stream. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.

## -parameters

### -param ulIndex [in]

Specifies the text selections that start the process. If the <a href="/windows/desktop/TSF/miscellaneous-framework-constants">TF_DEFAULT_SELECTION</a> constant is specified for this parameter, the input selection starts the process, and only a single selection (the one appropriate for input operations) will be returned.

### -param ulCount [in]

Specifies the maximum number of selections to return.

### -param pSelection [out]

Receives the style, start, and end character positions of the selected text. These values are put into the <a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_anchor">TS_SELECTION_ANCHOR</a> structure.

### -param pcFetched [out]

Receives the number of <i>pSelection</i> structures returned.

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
The method was unable to load the start or end anchor into the <b>TS_SELECTION_ANCHOR</b> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory for the selection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read-only lock on the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOSELECTION</b></dt>
</dl>
</td>
<td width="60%">
The document has no selection.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/TSF/edit-contexts">Edit Contexts</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-setselection">ITextStoreAnchor::SetSelection
      </a>



<a href="/windows/desktop/TSF/miscellaneous-framework-constants">Miscellaneous Framework Constants</a>



TF_DEFAULT_SELECTION



<a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_anchor">TS_SELECTION_ANCHOR
      </a>