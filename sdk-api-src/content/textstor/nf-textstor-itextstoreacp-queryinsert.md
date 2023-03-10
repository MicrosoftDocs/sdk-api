---
UID: NF:textstor.ITextStoreACP.QueryInsert
title: ITextStoreACP::QueryInsert (textstor.h)
description: The ITextStoreACP::QueryInsert method determines whether the specified start and end character positions are valid.
helpviewer_keywords: ["ITextStoreACP interface [Text Services Framework]","QueryInsert method","ITextStoreACP.QueryInsert","ITextStoreACP::QueryInsert","QueryInsert","QueryInsert method [Text Services Framework]","QueryInsert method [Text Services Framework]","ITextStoreACP interface","_tsf_itextstoreacp_queryinsert_ref","textstor/ITextStoreACP::QueryInsert","tsf.itextstoreacp_queryinsert"]
old-location: tsf\itextstoreacp_queryinsert.htm
tech.root: TSF
ms.assetid: e02846a2-d50c-4f1e-b44b-1dfa0bf50442
ms.date: 12/05/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],QueryInsert method, ITextStoreACP.QueryInsert, ITextStoreACP::QueryInsert, QueryInsert, QueryInsert method [Text Services Framework], QueryInsert method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_queryinsert_ref, textstor/ITextStoreACP::QueryInsert, tsf.itextstoreacp_queryinsert
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
 - ITextStoreACP::QueryInsert
 - textstor/ITextStoreACP::QueryInsert
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
 - ITextStoreACP.QueryInsert
---

# ITextStoreACP::QueryInsert


## -description

The <b>ITextStoreACP::QueryInsert</b> method determines whether the specified start and end character positions are valid. Use this method to adjust an edit to a document before executing the edit. The method must not return values outside the range of the document.

## -parameters

### -param acpTestStart [in]

Starting application character position for inserted text.

### -param acpTestEnd [in]

Ending application character position for the inserted text. This value is equal to <i>acpTextStart</i> if the text is inserted at a point instead of replacing selected text.

### -param cch [in]

Length of replacement text.

### -param pacpResultStart [out]

Returns the new starting application character position of the inserted text. If this parameter is <b>NULL</b>, then text cannot be inserted at the specified position. This value cannot be outside the document range.

### -param pacpResultEnd [out]

Returns the new ending application character position of the inserted text. If this parameter is <b>NULL</b>, then <i>pacpResultStart</i> is set to <b>NULL</b> and text cannot be inserted at the specified position. This value cannot be outside the document range.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>acpTestStart</i> or <i>acpTestEnd</i> parameters are invalid.

</td>
</tr>
</table>

## -remarks

The values of <i>pacpResultStart</i> and <i>pacpResultEnd</i> depend upon how the application inserts text into the document. If <i>pacpResultStart</i> and <i>pacpResultEnd</i> are the same as <i>acpTextStart</i>, the cursor is at the beginning of the inserted text after insertion. If <i>pacpResultStart</i> and <i>pacpResultEnd</i> are the same as <i>acpTextEnd</i>, the cursor is at the end of the inserted text after insertion. If the difference between <i>pacpResultStart</i> and <i>pacpResultEnd</i> is equal to the length of the inserted text, the inserted text is highlighted after insertion.

