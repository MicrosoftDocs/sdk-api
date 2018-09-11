---
UID: NF:textstor.ITextStoreAnchorSink.OnLockGranted
title: ITextStoreAnchorSink::OnLockGranted
author: windows-sdk-content
description: ITextStoreAnchorSink::OnLockGranted method
old-location: tsf\itextstoreanchorsink_onlockgranted.htm
tech.root: TSF
ms.assetid: 4a2ab828-1eb8-4aae-bebd-dc8b406fd58f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnLockGranted method, ITextStoreAnchorSink.OnLockGranted, ITextStoreAnchorSink::OnLockGranted, OnLockGranted, OnLockGranted method [Text Services Framework], OnLockGranted method [Text Services Framework],ITextStoreAnchorSink interface, TS_LF_READ, TS_LF_READWRITE, _tsf_itextstoreanchorsink_onlockgranted_ref, textstor/ITextStoreAnchorSink::OnLockGranted, tsf.itextstoreanchorsink_onlockgranted
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITextStoreAnchorSink.OnLockGranted
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchorSink::OnLockGranted


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



A document lock is requested by calling <a href="https://msdn.microsoft.com/4cace5bd-d111-4a9a-af10-9ad454d4f2eb">ITextStoreAnchor::RequestLock</a>. The application grants the lock request by calling <b>ITextStoreAnchorSink::OnLockGranted</b> with the requested lock type. The lock is only valid during the <b>OnLockGranted</b> call. When <b>OnLockGranted</b> returns, the document is considered unlocked.

The lock type, specified in <i>dwLockFlags</i>, must match the requested lock type in the corresponding call to <b>ITextStoreAnchor::RequestLock</b>.

Calls to <b>ITextStoreAnchor::RequestLock</b> from within <b>OnLockGranted</b> will return an error value.

Applications must not call any of the <a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink</a> methods from within the context of <b>OnLockGranted</b>.

If a synchronous lock request is made from within <b>ITextStoreAnchor::RequestLock</b>, then the caller must also provide the return value from <b>ITextStoreAnchor::RequestLock</b>.




## -see-also




<a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">Document Locks</a>



<a href="https://msdn.microsoft.com/4cace5bd-d111-4a9a-af10-9ad454d4f2eb">ITextStoreAnchor::RequestLock
      </a>



<a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink
      </a>



<a href="https://msdn.microsoft.com/f0bb6ef9-a8fc-4331-9210-6c5ba1721a73">TS_LF_* Constants
      </a>
 

 

