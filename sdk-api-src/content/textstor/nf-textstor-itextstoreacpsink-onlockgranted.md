---
UID: NF:textstor.ITextStoreACPSink.OnLockGranted
title: ITextStoreACPSink::OnLockGranted (textstor.h)
description: ITextStoreACPSink::OnLockGranted method
helpviewer_keywords: ["ITextStoreACPSink interface [Text Services Framework]","OnLockGranted method","ITextStoreACPSink.OnLockGranted","ITextStoreACPSink::OnLockGranted","OnLockGranted","OnLockGranted method [Text Services Framework]","OnLockGranted method [Text Services Framework]","ITextStoreACPSink interface","TS_LF_READ","TS_LF_READWRITE","_tsf_itextstoreacpsink_onlockgranted_ref","textstor/ITextStoreACPSink::OnLockGranted","tsf.itextstoreacpsink_onlockgranted"]
old-location: tsf\itextstoreacpsink_onlockgranted.htm
tech.root: TSF
ms.assetid: ddedd278-ec28-417e-bce2-cdb74db7b0f3
ms.date: 12/05/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnLockGranted method, ITextStoreACPSink.OnLockGranted, ITextStoreACPSink::OnLockGranted, OnLockGranted, OnLockGranted method [Text Services Framework], OnLockGranted method [Text Services Framework],ITextStoreACPSink interface, TS_LF_READ, TS_LF_READWRITE, _tsf_itextstoreacpsink_onlockgranted_ref, textstor/ITextStoreACPSink::OnLockGranted, tsf.itextstoreacpsink_onlockgranted
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
 - ITextStoreACPSink::OnLockGranted
 - textstor/ITextStoreACPSink::OnLockGranted
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
 - ITextStoreACPSink.OnLockGranted
---

# ITextStoreACPSink::OnLockGranted


## -description

Called to grant a document lock.

## -parameters

### -param dwLockFlags [in]

Contains a set of flags that identify the type of lock requested and other lock request data. This can be one of the following values.

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
The lock is read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_LF_READWRITE"></a><a id="ts_lf_readwrite"></a><dl>
<dt><b>TS_LF_READWRITE</b></dt>
</dl>
</td>
<td width="60%">
The lock is read/write.

</td>
</tr>
</table>

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
<i>dwLockFlags</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The wrong type of lock was granted.

</td>
</tr>
</table>

## -remarks

A document lock is requested by calling <b>ITextStoreACP::RequestLock</b> . The application grants the lock request by calling <b>ITextStoreACPSink::OnLockGranted</b> with the requested lock type. The lock is only valid during the <b>OnLockGranted</b> call. When <b>OnLockGranted</b> returns, the document is considered unlocked.

The lock type, specified in <i>dwLockFlags</i>, must match the requested lock type in the corresponding call to <b>ITextStoreACP::RequestLock</b>.

If a synchronous lock request is made from within <b>ITextStoreACP::RequestLock</b>, then the caller must also provide the return value from <b>ITextStoreACP::RequestLock</b>.

## -see-also

<a href="/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestlock">ITextStoreACP::RequestLock
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacpsink">ITextStoreACPSink</a>



<a href="/windows/desktop/TSF/ts-lf--constants">TS_LF_* Constants
      </a>