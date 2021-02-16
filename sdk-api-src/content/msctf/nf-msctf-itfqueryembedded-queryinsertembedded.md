---
UID: NF:msctf.ITfQueryEmbedded.QueryInsertEmbedded
title: ITfQueryEmbedded::QueryInsertEmbedded (msctf.h)
description: ITfQueryEmbedded::QueryInsertEmbedded method
helpviewer_keywords: ["ITfQueryEmbedded interface [Text Services Framework]","QueryInsertEmbedded method","ITfQueryEmbedded.QueryInsertEmbedded","ITfQueryEmbedded::QueryInsertEmbedded","QueryInsertEmbedded","QueryInsertEmbedded method [Text Services Framework]","QueryInsertEmbedded method [Text Services Framework]","ITfQueryEmbedded interface","_tsf_itfqueryembedded_queryinsertembedded_ref","msctf/ITfQueryEmbedded::QueryInsertEmbedded","tsf.itfqueryembedded_queryinsertembedded"]
old-location: tsf\itfqueryembedded_queryinsertembedded.htm
tech.root: TSF
ms.assetid: 52f9465f-725e-493b-89ee-1b3db3cef696
ms.date: 12/05/2018
ms.keywords: ITfQueryEmbedded interface [Text Services Framework],QueryInsertEmbedded method, ITfQueryEmbedded.QueryInsertEmbedded, ITfQueryEmbedded::QueryInsertEmbedded, QueryInsertEmbedded, QueryInsertEmbedded method [Text Services Framework], QueryInsertEmbedded method [Text Services Framework],ITfQueryEmbedded interface, _tsf_itfqueryembedded_queryinsertembedded_ref, msctf/ITfQueryEmbedded::QueryInsertEmbedded, tsf.itfqueryembedded_queryinsertembedded
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfQueryEmbedded::QueryInsertEmbedded
 - msctf/ITfQueryEmbedded::QueryInsertEmbedded
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
 - ITfQueryEmbedded.QueryInsertEmbedded
---

# ITfQueryEmbedded::QueryInsertEmbedded


## -description

Determines if the active context can accept an embedded object.

## -parameters

### -param pguidService [in]

A GUID that identifies the service associated with the object. This value can be <b>NULL</b> if <i>pFormatEtc</i> is valid.

### -param pFormatEtc [in]

Pointer to a <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure that contains data about the object to be embedded. This value can be <b>NULL</b> if <i>pguidService</i> is valid.

### -param pfInsertable [out]

Pointer to a Boolean value that receives the query result. This value receives a nonzero value if the object can be embedded, or zero otherwise.

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
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
There is no active context.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfqueryembedded">ITfQueryEmbedded</a>



<a href="/windows/desktop/com/the-formatetc-structure">The FORMATETC Structure</a>