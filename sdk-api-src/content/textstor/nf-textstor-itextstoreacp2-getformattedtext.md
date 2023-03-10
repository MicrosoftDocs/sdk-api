---
UID: NF:textstor.ITextStoreACP2.GetFormattedText
title: ITextStoreACP2::GetFormattedText (textstor.h)
description: Gets formatted text data about a specified text string. The caller must have a read/write lock on the document before calling this method.
helpviewer_keywords: ["GetFormattedText","GetFormattedText method [Text Services Framework]","GetFormattedText method [Text Services Framework]","ITextStoreACP2 interface","ITextStoreACP2 interface [Text Services Framework]","GetFormattedText method","ITextStoreACP2.GetFormattedText","ITextStoreACP2::GetFormattedText","textstor/ITextStoreACP2::GetFormattedText","tsf.itextstoreacp2_getformattedtext"]
old-location: tsf\itextstoreacp2_getformattedtext.htm
tech.root: TSF
ms.assetid: 0993861d-ef2a-4da5-a564-7559e7c4dcec
ms.date: 12/05/2018
ms.keywords: GetFormattedText, GetFormattedText method [Text Services Framework], GetFormattedText method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetFormattedText method, ITextStoreACP2.GetFormattedText, ITextStoreACP2::GetFormattedText, textstor/ITextStoreACP2::GetFormattedText, tsf.itextstoreacp2_getformattedtext
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
 - ITextStoreACP2::GetFormattedText
 - textstor/ITextStoreACP2::GetFormattedText
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
 - ITextStoreACP2.GetFormattedText
---

# ITextStoreACP2::GetFormattedText


## -description

Gets formatted text data about a specified text string. The caller must have a read/write lock on the document before calling this method.

## -parameters

### -param acpStart [in]

Specifies the starting character position of the text to get in the document.

### -param acpEnd [in]

Specifies the ending character position of the text to get in the document. This parameter is ignored if the value is 1.

### -param ppDataObject [out]

Receives the pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> object that contains the formatted text.

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
The caller does not have a read/write lock on the document.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>