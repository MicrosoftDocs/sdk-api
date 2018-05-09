---
UID: NF:msctf.ITfContext.RequestEditSession
title: ITfContext::RequestEditSession
author: windows-driver-content
description: ITfContext::RequestEditSession method
old-location: tsf\itfcontext_requesteditsession.htm
old-project: TSF
ms.assetid: 6c7b150c-0ca0-4aa5-8828-0c548dbfb215
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ITfContext interface [Text Services Framework],RequestEditSession method, ITfContext.RequestEditSession, ITfContext::RequestEditSession, RequestEditSession, RequestEditSession method [Text Services Framework], RequestEditSession method [Text Services Framework],ITfContext interface, TF_ES_ASYNC, TF_ES_ASYNCDONTCARE, TF_ES_READ, TF_ES_READWRITE, TF_ES_SYNC, _tsf_itfcontext_requesteditsession_ref, msctf/ITfContext::RequestEditSession, tsf.itfcontext_requesteditsession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfContext.RequestEditSession
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContext::RequestEditSession


## -description




## -parameters




### -param tid [in]

Contains a <a href="https://msdn.microsoft.com/984dc390-6e15-4491-8c06-77c27c5bdd6f">TfClientId</a> value that identifies the client to establish the edit session with.


### -param pes [in]

Pointer to an <a href="https://msdn.microsoft.com/b9d4718a-42a6-4be5-9f57-1a392cd98469">ITfEditSession</a> interface called to perform the edit session.


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
<li>If a synchronous edit session is established, receives the return value of the <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.</li>
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
<a href="https://msdn.microsoft.com/7763a879-a558-463d-837b-e38e6f84b9f7">
              ITfTextEditSink::OnEndEdit
            </a>
</li>
<li>
<a href="https://msdn.microsoft.com/a99313ab-98a7-4fc0-b3ae-78ff26a41d8e">
              ITfTextLayoutSink::OnLayoutChange
            </a>
</li>
<li>
<a href="https://msdn.microsoft.com/6eabf08f-006b-43b4-aea7-1d803b3d09b2">
              ITfStatusSink::OnStatusChange
            </a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a>



<a href="https://msdn.microsoft.com/b9d4718a-42a6-4be5-9f57-1a392cd98469">ITfEditSession
      </a>



<a href="https://msdn.microsoft.com/6eabf08f-006b-43b4-aea7-1d803b3d09b2">
        ITfStatusSink::OnStatusChange
      </a>



<a href="https://msdn.microsoft.com/7763a879-a558-463d-837b-e38e6f84b9f7">
        ITfTextEditSink::OnEndEdit
      </a>



<a href="https://msdn.microsoft.com/a99313ab-98a7-4fc0-b3ae-78ff26a41d8e">
        ITfTextLayoutSink::OnLayoutChange
      </a>
 

 

