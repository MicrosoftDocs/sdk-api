---
UID: NF:textstor.ITextStoreAnchorSink.OnTextChange
title: ITextStoreAnchorSink::OnTextChange (textstor.h)
description: ITextStoreAnchorSink::OnTextChange method
helpviewer_keywords: ["0","ITextStoreAnchorSink interface [Text Services Framework]","OnTextChange method","ITextStoreAnchorSink.OnTextChange","ITextStoreAnchorSink::OnTextChange","OnTextChange","OnTextChange method [Text Services Framework]","OnTextChange method [Text Services Framework]","ITextStoreAnchorSink interface","TS_TC_CORRECTION","_tsf_itextstoreanchorsink_ontextchange_ref","textstor/ITextStoreAnchorSink::OnTextChange","tsf.itextstoreanchorsink_ontextchange"]
old-location: tsf\itextstoreanchorsink_ontextchange.htm
tech.root: TSF
ms.assetid: 4bdf12bc-c15e-4bdb-8bc0-53172e9c943e
ms.date: 12/05/2018
ms.keywords: 0, ITextStoreAnchorSink interface [Text Services Framework],OnTextChange method, ITextStoreAnchorSink.OnTextChange, ITextStoreAnchorSink::OnTextChange, OnTextChange, OnTextChange method [Text Services Framework], OnTextChange method [Text Services Framework],ITextStoreAnchorSink interface, TS_TC_CORRECTION, _tsf_itextstoreanchorsink_ontextchange_ref, textstor/ITextStoreAnchorSink::OnTextChange, tsf.itextstoreanchorsink_ontextchange
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
 - ITextStoreAnchorSink::OnTextChange
 - textstor/ITextStoreAnchorSink::OnTextChange
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
 - ITextStoreAnchorSink.OnTextChange
---

# ITextStoreAnchorSink::OnTextChange


## -description

Called when text in the text stream changes.

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
<td width="40%"><a id="TS_TC_CORRECTION"></a><a id="ts_tc_correction"></a><dl>
<dt><b>TS_TC_CORRECTION</b></dt>
</dl>
</td>
<td width="60%">
The text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier. This flag is used for applications that need to preserve data associated with the original text.

</td>
</tr>
</table>

### -param paStart [in]

Pointer to an anchor located at the start of the changed text.

### -param paEnd [in]

Pointer to an anchor located at the end of the changed text.

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
The method was unable to create cloned anchors to contain the change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>paStart</i> or <i>paEnd</i> is invalid.

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
The TSF manager holds a lock on the document. This typically indicates that the method was called from within another <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a> method, such as <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-settext">ITextStoreAnchor::SetText</a>.

</td>
</tr>
</table>

## -remarks

This method is called only when the application modifies its own text, not when a client modifies text with one of the <b>ITextStoreAnchor</b> methods, such as <b>ITextStoreAnchor::SetText</b> or <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-inserttextatselection">ITextStoreAnchor::InsertTextAtSelection</a>.

When calling this method, the application must be able to grant a <a href="/windows/desktop/TSF/document-locks">document lock</a>.

## -see-also

<a href="/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-inserttextatselection">ITextStoreAnchor::InsertTextAtSelection
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-settext">ITextStoreAnchor::SetText
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchorsink">ITextStoreAnchorSink</a>



<a href="/windows/desktop/TSF/miscellaneous-text-store-constants">Miscellaneous Text Store Constants
      </a>