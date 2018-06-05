---
UID: NF:upnp.IUPnPServiceAsync.CancelAsyncOperation
title: IUPnPServiceAsync::CancelAsyncOperation
author: windows-sdk-content
description: CancelAsyncOperation method cancels a pending asynchronous operation initiated by the BeginInvokeAction, BeginQueryStateVariable, BeginSubscribeToEvents, or BeginSCPDDownload methods.
old-location: upnp\iupnpserviceasync_cancelasyncoperation.htm
old-project: UPnP
ms.assetid: FBEC2DF3-6D45-49F2-AAA8-6DED697BC5A6
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: CancelAsyncOperation, CancelAsyncOperation method [UPnP APIs], CancelAsyncOperation method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],CancelAsyncOperation method, IUPnPServiceAsync.CancelAsyncOperation, IUPnPServiceAsync::CancelAsyncOperation, upnp.iupnpserviceasync_cancelasyncoperation, upnp/IUPnPServiceAsync::CancelAsyncOperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Upnp.dll
api_name:
-	IUPnPServiceAsync.CancelAsyncOperation
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
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
 

 

