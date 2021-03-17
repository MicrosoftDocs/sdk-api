---
UID: NF:textstor.ITextStoreACP.GetFormattedText
title: ITextStoreACP::GetFormattedText (textstor.h)
description: The ITextStoreACP::GetFormattedText method returns formatted text data about a specified text string. The caller must have a read/write lock on the document before calling this method.
helpviewer_keywords: ["GetFormattedText","GetFormattedText method [Text Services Framework]","GetFormattedText method [Text Services Framework]","ITextStoreACP interface","ITextStoreACP interface [Text Services Framework]","GetFormattedText method","ITextStoreACP.GetFormattedText","ITextStoreACP::GetFormattedText","_tsf_itextstoreacp_getformattedtext_ref","textstor/ITextStoreACP::GetFormattedText","tsf.itextstoreacp_getformattedtext"]
old-location: tsf\itextstoreacp_getformattedtext.htm
tech.root: TSF
ms.assetid: 1c4e6f8d-d7c6-455d-8efe-7da8dfdd9c4b
ms.date: 12/05/2018
ms.keywords: GetFormattedText, GetFormattedText method [Text Services Framework], GetFormattedText method [Text Services Framework],ITextStoreACP interface, ITextStoreACP interface [Text Services Framework],GetFormattedText method, ITextStoreACP.GetFormattedText, ITextStoreACP::GetFormattedText, _tsf_itextstoreacp_getformattedtext_ref, textstor/ITextStoreACP::GetFormattedText, tsf.itextstoreacp_getformattedtext
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
 - ITextStoreACP::GetFormattedText
 - textstor/ITextStoreACP::GetFormattedText
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
 - ITextStoreACP.GetFormattedText
---

# ITextStoreACP::GetFormattedText


## -description

The <b>ITextStoreACP::GetFormattedText</b> method returns formatted text data about a specified text string. The caller must have a read/write lock on the document before calling this method.

## -parameters

### -param acpStart [in]

Specifies the starting character position of the text to get in the document.

### -param acpEnd [in]

Specifies the ending character position of the text to get in the document. This parameter is ignored if the value is 1.

### -param ppDataObject [out]

Receives the pointer to the <b>IDataObject</b> object that contains the formatted text.

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

