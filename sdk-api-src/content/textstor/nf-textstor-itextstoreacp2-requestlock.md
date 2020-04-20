---
UID: NF:textstor.ITextStoreACP2.RequestLock
title: ITextStoreACP2::RequestLock (textstor.h)
description: Called by the TSF manager to provide a document lock in order to modify the document. This method calls the OnLockGranted method to create the document lock.helpviewer_keywords: ["ITextStoreACP2 interface [Text Services Framework]","RequestLock method","ITextStoreACP2.RequestLock","ITextStoreACP2::RequestLock","RequestLock","RequestLock method [Text Services Framework]","RequestLock method [Text Services Framework]","ITextStoreACP2 interface","TS_LF_READ","TS_LF_READWRITE","TS_LF_SYNC","textstor/ITextStoreACP2::RequestLock","tsf.itextstoreacp2_requestlock"]
old-location: tsf\itextstoreacp2_requestlock.htm
tech.root: TSF
ms.assetid: 82254529-3deb-4e69-8571-3f8eaa533459
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],RequestLock method, ITextStoreACP2.RequestLock, ITextStoreACP2::RequestLock, RequestLock, RequestLock method [Text Services Framework], RequestLock method [Text Services Framework],ITextStoreACP2 interface, TS_LF_READ, TS_LF_READWRITE, TS_LF_SYNC, textstor/ITextStoreACP2::RequestLock, tsf.itextstoreacp2_requestlock
f1_keywords:
- textstor/ITextStoreACP2.RequestLock
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITextStoreACP2.RequestLock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextStoreACP2::RequestLock


## -description


Called by the TSF manager to provide a document lock in order to modify the document. This method calls the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlockgranted">OnLockGranted</a> method to create the document lock.


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

If the lock request is synchronous, receives an HRESULT value from the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlockgranted">OnLockGranted</a> method that specifies the result of the lock request.

If the lock request is asynchronous and the result is <a href="https://docs.microsoft.com/windows/desktop/TSF/text-store-return-values">TS_S_ASYNC</a>, the document receives an asynchronous lock. If the lock request is asynchronous and the result is TS_E_SYNCHRONOUS, the document can't be locked synchronously.


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



This method uses the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlockgranted">OnLockGranted</a> method to lock the document. Applications must never modify the document or send change notifications using the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-ontextchange">OnTextChange</a> method from within the <b>RequestLock</b> method. If the application has pending changes to report, the application can only respond to the asynchronous lock request.

Applications should not attempt to queue multiple <b>RequestLock</b> method calls, because the application requires only a single callback. If the caller makes several read requests and one or more write requests, however, the callback should be for write access.

Successful requests for synchronous locks supersede requests for asynchronous locks. Unsuccessful requests for synchronous locks do not supersede requests for asynchronous locks. The implementation must still serve the outstanding asynchronous request, if one exists.

If the lock is granted before the <b>RequestLock</b> method returns, the <i>phrSession</i> parameter will receive the HRESULT returned by the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlockgranted">OnLockGranted</a> method. If the call is successful, but the lock will be granted later, the <i>phrSession</i> parameter receives the TS_S_ASYNC flag. The <i>phrSession</i> parameter should be ignored if <b>RequestLock</b> returns anything other than S_OK.

A caller should never call this method reentrantly, except in the case that the caller holds a read-only lock. In this case the method can be called reentrantly to ask for an asynchronous write lock. The write lock will be granted later, after the read-only lock ends.

For more information about document locks, see <a href="https://docs.microsoft.com/windows/desktop/TSF/document-locks">Document Locks</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlockgranted">OnLockGranted</a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/ts-lf--constants">TS_LF_* Constants
      </a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/text-store-return-values">Text Store Return Values
      </a>
 

 

