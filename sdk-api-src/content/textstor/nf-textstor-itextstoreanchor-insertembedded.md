---
UID: NF:textstor.ITextStoreAnchor.InsertEmbedded
title: ITextStoreAnchor::InsertEmbedded (textstor.h)
description: ITextStoreAnchor::InsertEmbedded method
helpviewer_keywords: ["ITextStoreAnchor interface [Text Services Framework]","InsertEmbedded method","ITextStoreAnchor.InsertEmbedded","ITextStoreAnchor::InsertEmbedded","InsertEmbedded","InsertEmbedded method [Text Services Framework]","InsertEmbedded method [Text Services Framework]","ITextStoreAnchor interface","textstor/ITextStoreAnchor::InsertEmbedded","tsf.itextstoreanchor_insertembedded"]
old-location: tsf\itextstoreanchor_insertembedded.htm
tech.root: TSF
ms.assetid: 414842cc-7c3e-4f5c-93ac-3bd0eda5293e
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],InsertEmbedded method, ITextStoreAnchor.InsertEmbedded, ITextStoreAnchor::InsertEmbedded, InsertEmbedded, InsertEmbedded method [Text Services Framework], InsertEmbedded method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::InsertEmbedded, tsf.itextstoreanchor_insertembedded
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
 - ITextStoreAnchor::InsertEmbedded
 - textstor/ITextStoreAnchor::InsertEmbedded
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
 - ITextStoreAnchor.InsertEmbedded
---

# ITextStoreAnchor::InsertEmbedded


## -description

Inserts an IDataObject data object into a text stream.

## -parameters

### -param dwFlags [in]

Must be TS_IE_CORRECTION.

### -param paStart [in]

Pointer to the anchor at the start of the object to be inserted.

### -param paEnd [in]

Pointer to the anchor at the end of the object to be inserted.

### -param pDataObject [in]

Pointer to an <b>IDataObject</b> data object.

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
The method was unable to obtain a valid interface pointer to the start and/or end anchors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more input parameters are invalid.

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
<i>paStart</i> and/or <i>paEnd</i> are not within the document.

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



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-queryinsertembedded">ITextStoreAnchor::QueryInsertEmbedded
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-settext">ITextStoreAnchor::SetText
      </a>



<a href="/windows/desktop/TSF/ts-char--constants">TS_CHAR_EMBEDDED
      </a>



<a href="/windows/desktop/TSF/ts-ie--constants">TS_IE_* Constants
      </a>