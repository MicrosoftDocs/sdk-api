---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUPnPServiceAsync::CancelAsyncOperation


## -description


The <b>CancelAsyncOperation</b> method cancels a pending asynchronous operation initiated by the <a href="https://msdn.microsoft.com/40900CE1-03EE-451A-84DE-5C496EB2D7E5">BeginInvokeAction</a>, <a href="https://msdn.microsoft.com/1E97589C-A06B-4012-A2A2-C88BBE9B2530">BeginQueryStateVariable</a>,  <a href="https://msdn.microsoft.com/605629CB-9DBA-4130-B55D-957187551435">BeginSubscribeToEvents</a>, or <a href="https://msdn.microsoft.com/CA573855-6D86-4C6C-B557-F8E8776BDBD3">BeginSCPDDownload</a> methods.


## -parameters




### -param ullRequestID [in]

A 64-bit <b>ULONG</b> value that corresponds to the pending asynchronous UPnP operation.


## -returns



Returns <b>S_OK</b> on success. Otherwise, the method returns a COM error code defined in <b>WinError.h</b> or one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to cancel the asynchronous operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ullRequestID</i> does not match the pending asynchronous call.

</td>
</tr>
</table>
 




## -remarks



Calling this method for a pending <a href="https://msdn.microsoft.com/CA573855-6D86-4C6C-B557-F8E8776BDBD3">BeginSCPDDownload</a> operation the SCPD download will still take place in the background, but will not notify callbacks of events associated with the operation.




## -see-also




<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>



<a href="https://msdn.microsoft.com/40900CE1-03EE-451A-84DE-5C496EB2D7E5">IUPnPServiceAsync::BeginInvokeAction</a>



<a href="https://msdn.microsoft.com/1E97589C-A06B-4012-A2A2-C88BBE9B2530">IUPnPServiceAsync::BeginQueryStateVariable</a>



<a href="https://msdn.microsoft.com/CA573855-6D86-4C6C-B557-F8E8776BDBD3">IUPnPServiceAsync::BeginSCPDDownload</a>



<a href="https://msdn.microsoft.com/605629CB-9DBA-4130-B55D-957187551435">IUPnPServiceAsync::BeginSubscribeToEvents</a>
 

 

