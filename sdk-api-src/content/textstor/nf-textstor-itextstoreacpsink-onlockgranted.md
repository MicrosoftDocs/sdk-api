---
UID: NF:textstor.ITextStoreACPSink.OnLockGranted
title: ITextStoreACPSink::OnLockGranted (textstor.h)
author: windows-sdk-content
description: ITextStoreACPSink::OnLockGranted method
old-location: tsf\itextstoreacpsink_onlockgranted.htm
tech.root: TSF
ms.assetid: ddedd278-ec28-417e-bce2-cdb74db7b0f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnLockGranted method, ITextStoreACPSink.OnLockGranted, ITextStoreACPSink::OnLockGranted, OnLockGranted, OnLockGranted method [Text Services Framework], OnLockGranted method [Text Services Framework],ITextStoreACPSink interface, TS_LF_READ, TS_LF_READWRITE, _tsf_itextstoreacpsink_onlockgranted_ref, textstor/ITextStoreACPSink::OnLockGranted, tsf.itextstoreacpsink_onlockgranted
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACPSink.OnLockGranted
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreACPSink::OnLockGranted


## -description




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




<a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">Document Locks</a>



<a href="https://msdn.microsoft.com/ddd2b1f4-47de-4e87-be94-eea694ecd1b8">ITextStoreACP::RequestLock
      </a>



<a href="https://msdn.microsoft.com/d7e5a04f-7159-436e-a522-4cb63063aeef">ITextStoreACPSink</a>



<a href="https://msdn.microsoft.com/f0bb6ef9-a8fc-4331-9210-6c5ba1721a73">TS_LF_* Constants
      </a>
 

 

