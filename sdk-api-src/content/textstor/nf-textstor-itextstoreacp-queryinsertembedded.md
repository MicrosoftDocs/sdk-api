---
UID: NF:textstor.ITextStoreACP.QueryInsertEmbedded
title: ITextStoreACP::QueryInsertEmbedded (textstor.h)
description: Gets a value indicating whether the specified object can be inserted into the document. (ITextStoreACP.QueryInsertEmbedded)
helpviewer_keywords: ["ITextStoreACP interface [Text Services Framework]","QueryInsertEmbedded method","ITextStoreACP.QueryInsertEmbedded","ITextStoreACP::QueryInsertEmbedded","QueryInsertEmbedded","QueryInsertEmbedded method [Text Services Framework]","QueryInsertEmbedded method [Text Services Framework]","ITextStoreACP interface","_tsf_itextstoreacp_queryinsertembedded_ref","textstor/ITextStoreACP::QueryInsertEmbedded","tsf.itextstoreacp_queryinsertembedded"]
old-location: tsf\itextstoreacp_queryinsertembedded.htm
tech.root: TSF
ms.assetid: b1cf6162-da57-4b8a-beca-fb1ec390c577
ms.date: 12/05/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],QueryInsertEmbedded method, ITextStoreACP.QueryInsertEmbedded, ITextStoreACP::QueryInsertEmbedded, QueryInsertEmbedded, QueryInsertEmbedded method [Text Services Framework], QueryInsertEmbedded method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_queryinsertembedded_ref, textstor/ITextStoreACP::QueryInsertEmbedded, tsf.itextstoreacp_queryinsertembedded
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
 - ITextStoreACP::QueryInsertEmbedded
 - textstor/ITextStoreACP::QueryInsertEmbedded
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
 - ITextStoreACP.QueryInsertEmbedded
---

# ITextStoreACP::QueryInsertEmbedded


## -description

Gets a value indicating whether the specified object can be inserted into the document.

## -parameters

### -param pguidService [in]

Pointer to the object type. Can be <b>NULL</b>.

### -param pFormatEtc [in]

Pointer to the <a href="/windows/desktop/com/the-formatetc-structure">FORMATETC</a> structure that contains format data of the object. This parameter cannot be <b>NULL</b> if the <i>pguidService</i> parameter is <b>NULL</b>.

### -param pfInsertable [out]

Receives <b>TRUE</b> if the object type can be inserted into the document or <b>FALSE</b> if the object type cannot be inserted into the document.

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

<a href="/windows/desktop/com/the-formatetc-structure">FORMATETC</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded">ITextStoreACP::InsertEmbedded
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembeddedatselection">ITextStoreACP::InsertEmbeddedAtSelection
      </a>
