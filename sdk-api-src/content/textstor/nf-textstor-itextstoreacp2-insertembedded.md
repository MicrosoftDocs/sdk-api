---
UID: NF:textstor.ITextStoreACP2.InsertEmbedded
title: ITextStoreACP2::InsertEmbedded (textstor.h)
description: Inserts an embedded object at the specified character. (ITextStoreACP2.InsertEmbedded)
helpviewer_keywords: ["ITextStoreACP2 interface [Text Services Framework]","InsertEmbedded method","ITextStoreACP2.InsertEmbedded","ITextStoreACP2::InsertEmbedded","InsertEmbedded","InsertEmbedded method [Text Services Framework]","InsertEmbedded method [Text Services Framework]","ITextStoreACP2 interface","textstor/ITextStoreACP2::InsertEmbedded","tsf.itextstoreacp2_insertembedded"]
old-location: tsf\itextstoreacp2_insertembedded.htm
tech.root: TSF
ms.assetid: 1f5003e0-0d6d-4212-beea-3b2685991749
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],InsertEmbedded method, ITextStoreACP2.InsertEmbedded, ITextStoreACP2::InsertEmbedded, InsertEmbedded, InsertEmbedded method [Text Services Framework], InsertEmbedded method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::InsertEmbedded, tsf.itextstoreacp2_insertembedded
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
 - ITextStoreACP2::InsertEmbedded
 - textstor/ITextStoreACP2::InsertEmbedded
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
 - ITextStoreACP2.InsertEmbedded
---

# ITextStoreACP2::InsertEmbedded


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



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/TSF/ts-ie--constants">TS_IE_* Constants
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE
      </a>
