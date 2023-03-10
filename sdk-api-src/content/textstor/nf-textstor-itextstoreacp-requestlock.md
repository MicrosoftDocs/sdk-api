---
UID: NF:textstor.ITextStoreACP.RequestLock
title: ITextStoreACP::RequestLock (textstor.h)
description: The ITextStoreACP::RequestLock method is called by the TSF manager to provide a document lock in order to modify the document. This method calls the ITextStoreACPSink::OnLockGranted method to create the document lock.
helpviewer_keywords: ["ITextStoreACP interface [Text Services Framework]","RequestLock method","ITextStoreACP.RequestLock","ITextStoreACP::RequestLock","RequestLock","RequestLock method [Text Services Framework]","RequestLock method [Text Services Framework]","ITextStoreACP interface","TS_LF_READ","TS_LF_READWRITE","TS_LF_SYNC","_tsf_itextstoreacp_requestlock_ref","textstor/ITextStoreACP::RequestLock","tsf.itextstoreacp_requestlock"]
old-location: tsf\itextstoreacp_requestlock.htm
tech.root: TSF
ms.assetid: ddd2b1f4-47de-4e87-be94-eea694ecd1b8
ms.date: 12/05/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],RequestLock method, ITextStoreACP.RequestLock, ITextStoreACP::RequestLock, RequestLock, RequestLock method [Text Services Framework], RequestLock method [Text Services Framework],ITextStoreACP interface, TS_LF_READ, TS_LF_READWRITE, TS_LF_SYNC, _tsf_itextstoreacp_requestlock_ref, textstor/ITextStoreACP::RequestLock, tsf.itextstoreacp_requestlock
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
 - ITextStoreACP::RequestLock
 - textstor/ITextStoreACP::RequestLock
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
 - ITextStoreACP.RequestLock
---

# ITextStoreACP::RequestLock


## -description

The <b>ITextStoreACP::RequestLock</b> method is called by the TSF manager to provide a document lock in order to modify the document. This method calls the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlockgranted">ITextStoreACPSink::OnLockGranted</a> method to create the document lock.

## -parameters

### -param dwLockFlags [in]

Specifies the type of lock requested.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TS_LF_READ"></a><a id="ts_lf_read"></a><dl>
<dt><b>TS_LF_READ</b></dt>
</dl>
</td>
<td width="60%">
The document has a read-only lock and cannot be modified.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_LF_READWRITE"></a><a id="ts_lf_readwrite"></a><dl>
<dt><b>TS_LF_READWRITE</b></dt>
</dl>
</td>
<td width="60%">
The document has a read/write lock and can be modified.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_LF_SYNC"></a><a id="ts_lf_sync"></a><dl>
<dt><b>TS_LF_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The document has a synchronous-lock if this flag is combined with other flags.

</td>
</tr>
</table>

### -param phrSession [out]

If the lock request is synchronous, receives an HRESULT value from the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onlockgranted">ITextStoreAnchorSink::OnLockGranted</a> method that specifies the result of the lock request.

If the lock request is asynchronous and the result is <a href="/windows/desktop/TSF/text-store-return-values">TS_S_ASYNC</a>, the document receives an asynchronous lock. If the lock request is asynchronous and the result is TS_E_SYNCHRONOUS, the document cannot be locked synchronously.

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
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

This method uses the <b>ITextStoreACPSink::OnLockGranted</b> method to lock the document. Applications must never modify the document or send change notifications using the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-ontextchange">ITextStoreACPSink::OnTextChange</a> method from within the <b>ITextStoreACP::RequestLock</b> method. If the application has pending changes to report, the application can only respond to the asynchronous lock request.

Applications should not attempt to queue multiple <b>ITextStoreACP::RequestLock</b> method calls, because the application requires only a single callback. If the caller makes several read requests and one or more write requests, however, the callback should be for write access.

Successful requests for synchronous locks supersede requests for asynchronous locks. Unsuccessful requests for synchronous locks do not supersede requests for asynchronous locks. The implementation must still serve the outstanding asynchronous request, if one exists.

If the lock is granted before the <b>ITextStoreACP::RequestLock</b> method returns, the <i>phrSession</i> parameter will receive the HRESULT returned by the <b>ITextStoreACPSink::OnLockGranted</b> method. If the call is successful, but the lock will be granted later, the <i>phrSession</i> parameter receives the TS_S_ASYNC flag. The <i>phrSession</i> parameter should be ignored if <b>ITextStoreACP::RequestLock</b> returns anything other than S_OK.

A caller should never call this method reentrantly, except in the case that the caller holds a read-only lock. In this case the method can be called reentrantly to ask for an asynchronous write lock. The write lock will be granted later, after the read-only lock ends.

For more information about document locks, see <a href="/windows/desktop/TSF/document-locks">Document Locks</a>.

## -see-also

<a href="/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlockgranted">ITextStoreACPSink::OnLockGranted
      </a>



<a href="/windows/desktop/TSF/ts-lf--constants">TS_LF_* Constants
      </a>



<a href="/windows/desktop/TSF/text-store-return-values">Text Store Return Values
      </a>