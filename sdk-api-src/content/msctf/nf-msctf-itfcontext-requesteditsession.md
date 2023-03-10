---
UID: NF:msctf.ITfContext.RequestEditSession
title: ITfContext::RequestEditSession (msctf.h)
description: ITfContext::RequestEditSession method
helpviewer_keywords: ["ITfContext interface [Text Services Framework]","RequestEditSession method","ITfContext.RequestEditSession","ITfContext::RequestEditSession","RequestEditSession","RequestEditSession method [Text Services Framework]","RequestEditSession method [Text Services Framework]","ITfContext interface","TF_ES_ASYNC","TF_ES_ASYNCDONTCARE","TF_ES_READ","TF_ES_READWRITE","TF_ES_SYNC","_tsf_itfcontext_requesteditsession_ref","msctf/ITfContext::RequestEditSession","tsf.itfcontext_requesteditsession"]
old-location: tsf\itfcontext_requesteditsession.htm
tech.root: TSF
ms.assetid: 6c7b150c-0ca0-4aa5-8828-0c548dbfb215
ms.date: 12/05/2018
ms.keywords: ITfContext interface [Text Services Framework],RequestEditSession method, ITfContext.RequestEditSession, ITfContext::RequestEditSession, RequestEditSession, RequestEditSession method [Text Services Framework], RequestEditSession method [Text Services Framework],ITfContext interface, TF_ES_ASYNC, TF_ES_ASYNCDONTCARE, TF_ES_READ, TF_ES_READWRITE, TF_ES_SYNC, _tsf_itfcontext_requesteditsession_ref, msctf/ITfContext::RequestEditSession, tsf.itfcontext_requesteditsession
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITfContext::RequestEditSession
 - msctf/ITfContext::RequestEditSession
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
 - ITfContext.RequestEditSession
---

# ITfContext::RequestEditSession


## -description

Obtains access to the document text and properties.

## -parameters

### -param tid [in]

Contains a <a href="/windows/desktop/TSF/tfclientid">TfClientId</a> value that identifies the client to establish the edit session with.

### -param pes [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfeditsession">ITfEditSession</a> interface called to perform the edit session.

### -param dwFlags [in]

Contains one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_ES_ASYNCDONTCARE"></a><a id="tf_es_asyncdontcare"></a><dl>
<dt><b>TF_ES_ASYNCDONTCARE</b></dt>
</dl>
</td>
<td width="60%">
The edit session can occur synchronously or asynchronously, at the discretion of the TSF manager. The manager will attempt to schedule a synchronous edit session for improved performance. This value cannot be combined with the TF_ES_ASYNC or TF_ES_SYNC values.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_ES_SYNC"></a><a id="tf_es_sync"></a><dl>
<dt><b>TF_ES_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The edit session must be synchronous or the request will fail (with TF_E_SYNCHRONOUS). This flag should only be used in documented situations (such as keystroke handling) where it can be expected to succeed. Otherwise the call will likely fail. This value cannot be combined with the TF_ES_ASYNCDONTCARE or TF_ES_ASYNC values.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_ES_READ"></a><a id="tf_es_read"></a><dl>
<dt><b>TF_ES_READ</b></dt>
</dl>
</td>
<td width="60%">
Requests read-only access to the context.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_ES_READWRITE"></a><a id="tf_es_readwrite"></a><dl>
<dt><b>TF_ES_READWRITE</b></dt>
</dl>
</td>
<td width="60%">
Requests read/write access to the context.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_ES_ASYNC"></a><a id="tf_es_async"></a><dl>
<dt><b>TF_ES_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The edit session must be asynchronous or the request fails. This value cannot be combined with the TF_ES_ASYNCDONTCARE or TF_ES_SYNC values.

</td>
</tr>
</table>

### -param phrSession [out]

Address of an <b>HRESULT</b> value that receives the result of the edit session request. The value received depends upon the type of edit session requested.

<ul>
<li>If an asynchronous edit session is requested and can be established, receives TF_S_ASYNC.</li>
<li>If a synchronous edit session is requested and cannot be established, receives TF_E_SYNCHRONOUS.</li>
<li>If the TF_ES_READWRITE flag is specified and the document is read-only, receives TS_E_READONLY.</li>
<li>If a synchronous edit session is established, receives the return value of the <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.</li>
</ul>

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
The method was successful. <i>phrSession</i> contains more result data for the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The caller is within the context of another text service which already holds a lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context is not on a document stack.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

Pending asynchronous edit sessions are processed in the order received. Synchronous edit sessions are processed before any pending asynchronous edit sessions.

A text service can request an edit session within the context of an existing edit session, provided a write access session is not requested within a read-only session. Calls to this method within the context of an edit session established by another text service will fail with TF_E_LOCKED.

A synchronous read/write request will fail if made when processing one of the following notifications.

<ul>
<li>
<a href="/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit
            </a>
</li>
<li>
<a href="/windows/desktop/api/msctf/nf-msctf-itftextlayoutsink-onlayoutchange">ITfTextLayoutSink::OnLayoutChange
            </a>
</li>
<li>
<a href="/windows/desktop/api/msctf/nf-msctf-itfstatussink-onstatuschange">ITfStatusSink::OnStatusChange
            </a>
</li>
</ul>

## -see-also

[ITfContext interface](nn-msctf-itfcontext.md), [ITfEditSession interface](nn-msctf-itfeditsession.md), [ITfStatusSink::OnStatusChange](nf-msctf-itfstatussink-onstatuschange.md), [ITfTextEditSink::OnEndEdit](nf-msctf-itftexteditsink-onendedit.md), [ITfTextLayoutSink::OnLayoutChange](nf-msctf-itftextlayoutsink-onlayoutchange.md)