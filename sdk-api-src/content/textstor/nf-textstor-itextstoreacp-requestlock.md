---
UID: NF:textstor.ITextStoreACP.RequestLock
title: ITextStoreACP::RequestLock
author: windows-sdk-content
description: The ITextStoreACP::RequestLock method is called by the TSF manager to provide a document lock in order to modify the document. This method calls the ITextStoreACPSink::OnLockGranted method to create the document lock.
old-location: tsf\itextstoreacp_requestlock.htm
old-project: TSF
ms.assetid: ddd2b1f4-47de-4e87-be94-eea694ecd1b8
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],RequestLock method, ITextStoreACP.RequestLock, ITextStoreACP::RequestLock, RequestLock, RequestLock method [Text Services Framework], RequestLock method [Text Services Framework],ITextStoreACP interface, TS_LF_READ, TS_LF_READWRITE, TS_LF_SYNC, _tsf_itextstoreacp_requestlock_ref, textstor/ITextStoreACP::RequestLock, tsf.itextstoreacp_requestlock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreACP.RequestLock
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP::RequestLock


## -description


The <b>ITextStoreACP::RequestLock</b> method is called by the TSF manager to provide a document lock in order to modify the document. This method calls the <a href="https://msdn.microsoft.com/ddedd278-ec28-417e-bce2-cdb74db7b0f3">ITextStoreACPSink::OnLockGranted</a> method to create the document lock.


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

If the lock request is synchronous, receives an HRESULT value from the <a href="https://msdn.microsoft.com/4a2ab828-1eb8-4aae-bebd-dc8b406fd58f">ITextStoreAnchorSink::OnLockGranted</a> method that specifies the result of the lock request.

If the lock request is asynchronous and the result is <a href="https://msdn.microsoft.com/20b0a89f-ab52-466f-9669-c6c29ad12de0">TS_S_ASYNC</a>, the document receives an asynchronous lock. If the lock request is asynchronous and the result is TS_E_SYNCHRONOUS, the document cannot be locked synchronously.


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



This method uses the <b>ITextStoreACPSink::OnLockGranted</b> method to lock the document. Applications must never modify the document or send change notifications using the <a href="https://msdn.microsoft.com/ed11ebb8-312b-40c7-90de-f5aa7591afd2">ITextStoreACPSink::OnTextChange</a> method from within the <b>ITextStoreACP::RequestLock</b> method. If the application has pending changes to report, the application can only respond to the asynchronous lock request.

Applications should not attempt to queue multiple <b>ITextStoreACP::RequestLock</b> method calls, because the application requires only a single callback. If the caller makes several read requests and one or more write requests, however, the callback should be for write access.

Successful requests for synchronous locks supersede requests for asynchronous locks. Unsuccessful requests for synchronous locks do not supersede requests for asynchronous locks. The implementation must still serve the outstanding asynchronous request, if one exists.

If the lock is granted before the <b>ITextStoreACP::RequestLock</b> method returns, the <i>phrSession</i> parameter will receive the HRESULT returned by the <b>ITextStoreACPSink::OnLockGranted</b> method. If the call is successful, but the lock will be granted later, the <i>phrSession</i> parameter receives the TS_S_ASYNC flag. The <i>phrSession</i> parameter should be ignored if <b>ITextStoreACP::RequestLock</b> returns anything other than S_OK.

A caller should never call this method reentrantly, except in the case that the caller holds a read-only lock. In this case the method can be called reentrantly to ask for an asynchronous write lock. The write lock will be granted later, after the read-only lock ends.

For more information about document locks, see <a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">Document Locks</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">Document Locks</a>



<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/ddedd278-ec28-417e-bce2-cdb74db7b0f3">ITextStoreACPSink::OnLockGranted
      </a>



<a href="https://msdn.microsoft.com/f0bb6ef9-a8fc-4331-9210-6c5ba1721a73">
        TS_LF_* Constants
      </a>



<a href="https://msdn.microsoft.com/20b0a89f-ab52-466f-9669-c6c29ad12de0">
        Text Store Return Values
      </a>
 

 

