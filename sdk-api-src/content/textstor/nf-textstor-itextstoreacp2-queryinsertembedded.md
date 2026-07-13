---
UID: NF:textstor.ITextStoreACP2.QueryInsertEmbedded
title: ITextStoreACP2::QueryInsertEmbedded (textstor.h)
description: Gets a value indicating whether the specified object can be inserted into the document. (ITextStoreACP2.QueryInsertEmbedded)
helpviewer_keywords: ["ITextStoreACP2 interface [Text Services Framework]","QueryInsertEmbedded method","ITextStoreACP2.QueryInsertEmbedded","ITextStoreACP2::QueryInsertEmbedded","QueryInsertEmbedded","QueryInsertEmbedded method [Text Services Framework]","QueryInsertEmbedded method [Text Services Framework]","ITextStoreACP2 interface","textstor/ITextStoreACP2::QueryInsertEmbedded","tsf.itextstoreacp2_queryinsertembedded"]
old-location: tsf\itextstoreacp2_queryinsertembedded.htm
tech.root: TSF
ms.assetid: af67d721-290b-412d-9d99-ea7d6406f33d
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],QueryInsertEmbedded method, ITextStoreACP2.QueryInsertEmbedded, ITextStoreACP2::QueryInsertEmbedded, QueryInsertEmbedded, QueryInsertEmbedded method [Text Services Framework], QueryInsertEmbedded method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::QueryInsertEmbedded, tsf.itextstoreacp2_queryinsertembedded
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
 - ITextStoreACP2::QueryInsertEmbedded
 - textstor/ITextStoreACP2::QueryInsertEmbedded
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
 - ITextStoreACP2.QueryInsertEmbedded
---

# ITextStoreACP2::QueryInsertEmbedded


## -description

Gets a value indicating whether the specified object can be inserted into the document.

## -parameters

### -param pguidService [in]

Pointer to the object type. Can be <b>NULL</b>.

### -param pFormatEtc [in]

Pointer to the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure that contains format data of the object. This parameter cannot be <b>NULL</b> if the <i>pguidService</i> parameter is <b>NULL</b>.

### -param pfInsertable [out]

Receives <b>TRUE</b> if the object type can be inserted into the document or <b>FALSE</b> if the object type can't be inserted into the document.

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
The <i>pFormatEtc</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The clipboard formats supported by the document are dependent on the application.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-insertembedded">InsertEmbedded</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-insertembeddedatselection">InsertEmbeddedAtSelection</a>
