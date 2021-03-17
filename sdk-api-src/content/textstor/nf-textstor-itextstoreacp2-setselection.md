---
UID: NF:textstor.ITextStoreACP2.SetSelection
title: ITextStoreACP2::SetSelection (textstor.h)
description: Selects text within the document. The application must have a read/write lock on the document before calling this method.
helpviewer_keywords: ["ITextStoreACP2 interface [Text Services Framework]","SetSelection method","ITextStoreACP2.SetSelection","ITextStoreACP2::SetSelection","SetSelection","SetSelection method [Text Services Framework]","SetSelection method [Text Services Framework]","ITextStoreACP2 interface","textstor/ITextStoreACP2::SetSelection","tsf.itextstoreacp2_setselection"]
old-location: tsf\itextstoreacp2_setselection.htm
tech.root: TSF
ms.assetid: 0ed72ddd-523e-476a-ba4c-bbfef9483015
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],SetSelection method, ITextStoreACP2.SetSelection, ITextStoreACP2::SetSelection, SetSelection, SetSelection method [Text Services Framework], SetSelection method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::SetSelection, tsf.itextstoreacp2_setselection
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
 - ITextStoreACP2::SetSelection
 - textstor/ITextStoreACP2::SetSelection
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
 - ITextStoreACP2.SetSelection
---

# ITextStoreACP2::SetSelection


## -description

Selects text within the document. The application must have a read/write lock on the document before calling this method.

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

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-getselection">GetSelection</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_selection_acp">TS_SELECTION_ACP</a>