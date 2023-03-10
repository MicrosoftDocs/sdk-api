---
UID: NF:textstor.ITextStoreACP2.GetSelection
title: ITextStoreACP2::GetSelection (textstor.h)
description: Gets the character position of a text selection in a document. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.
helpviewer_keywords: ["GetSelection","GetSelection method [Text Services Framework]","GetSelection method [Text Services Framework]","ITextStoreACP2 interface","ITextStoreACP2 interface [Text Services Framework]","GetSelection method","ITextStoreACP2.GetSelection","ITextStoreACP2::GetSelection","textstor/ITextStoreACP2::GetSelection","tsf.itextstoreacp2_getselection"]
old-location: tsf\itextstoreacp2_getselection.htm
tech.root: TSF
ms.assetid: 5f0c6265-7dba-4c59-94f9-36341f05c18d
ms.date: 12/05/2018
ms.keywords: GetSelection, GetSelection method [Text Services Framework], GetSelection method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetSelection method, ITextStoreACP2.GetSelection, ITextStoreACP2::GetSelection, textstor/ITextStoreACP2::GetSelection, tsf.itextstoreacp2_getselection
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2::GetSelection
 - textstor/ITextStoreACP2::GetSelection
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
 - ITextStoreACP2.GetSelection
---

# ITextStoreACP2::GetSelection


## -description

Gets the character position of a text selection in a document. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.

## -parameters

### -param ulIndex [in]

Specifies the text selections that start the process. If the <a href="/windows/desktop/TSF/miscellaneous-framework-constants">TF_DEFAULT_SELECTION</a> constant is specified for this parameter, the input selection starts the process.

### -param ulCount [in]

Specifies the maximum number of selections to return.

### -param pSelection [out]

Receives the style, start, and end character positions of the selected text. These values are put into the <a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_acp">TS_SELECTION_ACP</a> structure.

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



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-setselection">ITextStoreACP::SetSelection
      </a>



<a href="/windows/desktop/TSF/miscellaneous-framework-constants">Miscellaneous Framework Constants</a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_acp">TS_SELECTION_ACP
      </a>