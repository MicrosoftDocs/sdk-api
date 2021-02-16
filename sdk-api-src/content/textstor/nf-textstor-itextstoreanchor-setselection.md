---
UID: NF:textstor.ITextStoreAnchor.SetSelection
title: ITextStoreAnchor::SetSelection (textstor.h)
description: ITextStoreAnchor::SetSelection method
helpviewer_keywords: ["ITextStoreAnchor interface [Text Services Framework]","SetSelection method","ITextStoreAnchor.SetSelection","ITextStoreAnchor::SetSelection","SetSelection","SetSelection method [Text Services Framework]","SetSelection method [Text Services Framework]","ITextStoreAnchor interface","textstor/ITextStoreAnchor::SetSelection","tsf.itextstoreanchor_setselection"]
old-location: tsf\itextstoreanchor_setselection.htm
tech.root: TSF
ms.assetid: ce301fa4-d1dd-4470-b8b5-fc944afdc621
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],SetSelection method, ITextStoreAnchor.SetSelection, ITextStoreAnchor::SetSelection, SetSelection, SetSelection method [Text Services Framework], SetSelection method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::SetSelection, tsf.itextstoreanchor_setselection
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
 - ITextStoreAnchor::SetSelection
 - textstor/ITextStoreAnchor::SetSelection
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
 - ITextStoreAnchor.SetSelection
---

# ITextStoreAnchor::SetSelection


## -description

Selects text within the document.

## -parameters

### -param ulCount [in]

Specifies the number of text selections in <i>pSelection</i>.

### -param pSelection [in]

Specifies the style, start, and end character positions of the text selected through the <a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_anchor">TS_SELECTION_ANCHOR</a> structure. The start anchor member <b>paStart</b> of the structure must never follow the end anchor member <b>paEnd</b>, although they might be at the same location.

When <b>paStart</b> = <b>paEnd</b>, the method places a caret at the anchor location. There can be only one caret at a time in the text stream.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate sufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The anchor locations specified are beyond the text in the document.

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

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getselection">ITextStoreAnchor::GetSelection
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_anchor">TS_SELECTION_ANCHOR
      </a>