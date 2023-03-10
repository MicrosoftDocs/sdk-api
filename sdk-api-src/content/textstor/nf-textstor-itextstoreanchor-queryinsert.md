---
UID: NF:textstor.ITextStoreAnchor.QueryInsert
title: ITextStoreAnchor::QueryInsert (textstor.h)
description: The ITextStoreAnchor::QueryInsert method determines whether the specified start and end anchors are valid. Use this method to adjust an edit to a document before you execute the edit. The method must not return values outside the range of the document.
helpviewer_keywords: ["ITextStoreAnchor interface [Text Services Framework]","QueryInsert method","ITextStoreAnchor.QueryInsert","ITextStoreAnchor::QueryInsert","QueryInsert","QueryInsert method [Text Services Framework]","QueryInsert method [Text Services Framework]","ITextStoreAnchor interface","textstor/ITextStoreAnchor::QueryInsert","tsf.itextstoreanchor_queryinsert"]
old-location: tsf\itextstoreanchor_queryinsert.htm
tech.root: TSF
ms.assetid: 953b3f9c-63b7-4d62-accb-b07acfa97432
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],QueryInsert method, ITextStoreAnchor.QueryInsert, ITextStoreAnchor::QueryInsert, QueryInsert, QueryInsert method [Text Services Framework], QueryInsert method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::QueryInsert, tsf.itextstoreanchor_queryinsert
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
 - ITextStoreAnchor::QueryInsert
 - textstor/ITextStoreAnchor::QueryInsert
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
 - ITextStoreAnchor.QueryInsert
---

# ITextStoreAnchor::QueryInsert


## -description

The <b>ITextStoreAnchor::QueryInsert</b> method determines whether the specified start and end anchors are valid. Use this method to adjust an edit to a document before you execute the edit. The method must not return values outside the range of the document.

## -parameters

### -param paTestStart [in]

Receives a pointer to a start anchor for the inserted text.

### -param paTestEnd [in]

Receives a pointer to an end anchor for the inserted text. This is the same as <i>paTestStart</i> if the text is inserted at a point instead of replacing selected text.

### -param cch [in]

Length of replacement text.

### -param ppaResultStart [out]

Pointer to the new anchor object at the starting location for the inserted text. If the value of this parameter is <b>NULL</b>, then text cannot be inserted at the specified position. This anchor cannot be outside the document.

### -param ppaResultEnd [out]

Pointer to the new anchor object at the ending location for the inserted text. If the value of this parameter is <b>NULL</b>, then text cannot be inserted at the specified position. This anchor cannot be outside the document.

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
The <i>paTestStart</i> or <i>paTestEnd</i> parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The attempt to instantiate the <i>ppaResultStart</i> and/or <i>ppaResultEnd</i> anchors failed.

</td>
</tr>
</table>

## -remarks

The values of <i>ppaResultStart</i> and <i>ppaResultEnd</i> depend upon how the application inserts text into the document. If <i>ppaResultStart</i> and <i>ppaResultEnd</i> are the same as <i>paTestStart</i>, the cursor is at the beginning of the inserted text after insertion. If <i>ppaResultStart</i> and <i>ppaResultEnd</i> are the same as <i>paTextEnd</i>, the cursor is at the end of the inserted text after insertion.

