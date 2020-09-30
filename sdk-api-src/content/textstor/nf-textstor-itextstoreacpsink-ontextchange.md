---
UID: NF:textstor.ITextStoreACPSink.OnTextChange
title: ITextStoreACPSink::OnTextChange (textstor.h)
description: ITextStoreACPSink::OnTextChange method
helpviewer_keywords: ["0","ITextStoreACPSink interface [Text Services Framework]","OnTextChange method","ITextStoreACPSink.OnTextChange","ITextStoreACPSink::OnTextChange","OnTextChange","OnTextChange method [Text Services Framework]","OnTextChange method [Text Services Framework]","ITextStoreACPSink interface","TS_ST_CORRECTION","_tsf_itextstoreacpsink_ontextchange_ref","textstor/ITextStoreACPSink::OnTextChange","tsf.itextstoreacpsink_ontextchange"]
old-location: tsf\itextstoreacpsink_ontextchange.htm
tech.root: TSF
ms.assetid: ed11ebb8-312b-40c7-90de-f5aa7591afd2
ms.date: 12/05/2018
ms.keywords: 0, ITextStoreACPSink interface [Text Services Framework],OnTextChange method, ITextStoreACPSink.OnTextChange, ITextStoreACPSink::OnTextChange, OnTextChange, OnTextChange method [Text Services Framework], OnTextChange method [Text Services Framework],ITextStoreACPSink interface, TS_ST_CORRECTION, _tsf_itextstoreacpsink_ontextchange_ref, textstor/ITextStoreACPSink::OnTextChange, tsf.itextstoreacpsink_ontextchange
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
 - ITextStoreACPSink::OnTextChange
 - textstor/ITextStoreACPSink::OnTextChange
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
 - ITextStoreACPSink.OnTextChange
---

# ITextStoreACPSink::OnTextChange


## -description

Called when the text of a document changes.

## -parameters

### -param dwFlags [in]

Contains a set of flags that specify additional information about the text change. This can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The text has changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_ST_CORRECTION"></a><a id="ts_st_correction"></a><dl>
<dt><b>TS_ST_CORRECTION</b></dt>
</dl>
</td>
<td width="60%">
The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier. This flag is used for applications that need to preserve data associated with the original text.

</td>
</tr>
</table>

### -param pChange [in]

Pointer to a <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure that contains text change data.

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
<i>pChange</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The TSF manager holds a lock on the document. This typically indicates that the method was called from within another <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> method, such as <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-settext">ITextStoreACP::SetText</a>.

</td>
</tr>
</table>

## -remarks

<b>ITextStoreACPSink::OnTextChange</b> is never called when the text is modified by one of the <b>ITextStoreACP</b> interface methods, such as <b>ITextStoreACP::SetText</b> or <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-inserttextatselection">ITextStoreACP::InsertTextAtSelection</a>.

When calling this method, the application must be able to grant a <a href="/windows/desktop/TSF/document-locks">document lock</a>.

## -see-also

<a href="/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-inserttextatselection">ITextStoreACP::InsertTextAtSelection
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestlock">ITextStoreACP::RequestLock
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-settext">ITextStoreACP::SetText
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacpsink">ITextStoreACPSink</a>



<a href="/windows/desktop/TSF/miscellaneous-text-store-constants">Miscellaneous Text Store Constants
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE
      </a>