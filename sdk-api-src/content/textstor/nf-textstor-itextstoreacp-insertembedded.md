---
UID: NF:textstor.ITextStoreACP.InsertEmbedded
title: ITextStoreACP::InsertEmbedded (textstor.h)
description: Inserts an embedded object at the specified character. (ITextStoreACP.InsertEmbedded)
helpviewer_keywords: ["ITextStoreACP interface [Text Services Framework]","InsertEmbedded method","ITextStoreACP.InsertEmbedded","ITextStoreACP::InsertEmbedded","InsertEmbedded","InsertEmbedded method [Text Services Framework]","InsertEmbedded method [Text Services Framework]","ITextStoreACP interface","_tsf_itextstoreacp_insertembedded_ref","textstor/ITextStoreACP::InsertEmbedded","tsf.itextstoreacp_insertembedded"]
old-location: tsf\itextstoreacp_insertembedded.htm
tech.root: TSF
ms.assetid: 3d1612ee-1eb2-44c1-921e-a84af56a0790
ms.date: 12/05/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],InsertEmbedded method, ITextStoreACP.InsertEmbedded, ITextStoreACP::InsertEmbedded, InsertEmbedded, InsertEmbedded method [Text Services Framework], InsertEmbedded method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_insertembedded_ref, textstor/ITextStoreACP::InsertEmbedded, tsf.itextstoreacp_insertembedded
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
 - ITextStoreACP::InsertEmbedded
 - textstor/ITextStoreACP::InsertEmbedded
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
 - ITextStoreACP.InsertEmbedded
---

# ITextStoreACP::InsertEmbedded


## -description

Inserts an embedded object at the specified character.

## -parameters

### -param dwFlags [in]

Must be TS_IE_CORRECTION.

### -param acpStart [in]

Contains the starting character position where the object is inserted.

### -param acpEnd [in]

Contains the ending character position where the object is inserted.

### -param pDataObject [in]

Pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface that contains data about the object inserted.

### -param pChange [out]

Pointer to a <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure that receives data about the modified text.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application does not support embedded objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The application does not support the data type contained in <i>pDataObject</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
<i>acpStart</i> and/or <i>acpEnd</i> are not within the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read/write lock.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/TSF/ts-ie--constants">TS_IE_* Constants
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE
      </a>
