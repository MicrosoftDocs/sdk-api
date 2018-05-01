---
UID: NF:upnp.IUPnPServiceAsync.BeginSubscribeToEvents
title: IUPnPServiceAsync::BeginSubscribeToEvents method
author: windows-driver-content
description: BeginSubscribeToEvents initiates event subscription in asynchronous mode and registers the application callback with the UPnP framework.
old-location: upnp\iupnpserviceasync_beginsubscribetoevents.htm
old-project: UPnP
ms.assetid: 605629CB-9DBA-4130-B55D-957187551435
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: BeginSubscribeToEvents method [UPnP APIs], BeginSubscribeToEvents method [UPnP APIs], IUPnPServiceAsync interface, BeginSubscribeToEvents,IUPnPServiceAsync.BeginSubscribeToEvents, IUPnPServiceAsync, IUPnPServiceAsync interface [UPnP APIs], BeginSubscribeToEvents method, IUPnPServiceAsync::BeginSubscribeToEvents, upnp.iupnpserviceasync_beginsubscribetoevents, upnp/IUPnPServiceAsync::BeginSubscribeToEvents
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Upnp.dll
api_name:
-	IUPnPServiceAsync.BeginSubscribeToEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPServiceAsync::BeginSubscribeToEvents method


## -description


The <b>BeginSubscribeToEvents</b> initiates event subscription in asynchronous mode and  registers the application callback with the UPnP framework.


## -parameters




### -param pUnkCallback [in]

Specifies the reference to the interface object that contains the callback to register. This object must either support the <a href="https://msdn.microsoft.com/44515be4-891b-4f3d-a2c2-1699e468e708">IUPnPServiceCallback</a> interface or the <a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a> interface.


### -param pAsyncResult [in, optional]

Specifies a reference to <a href="https://msdn.microsoft.com/53854510-BB0C-41E6-8651-F34991B24D5E">IUPnPAsyncResult</a> object. When the <b>BeginSubscribeToEvents</b> call is complete, 
	UPnP will use the <a href="https://msdn.microsoft.com/C71C0A78-C3D1-4725-99E2-542786B03C8F">IUPnPAsyncResult::AsyncOperationComplete</a> method to notify the control point.



### -param pullRequestID [out]

Pointer to a 64-bit <b>ULONG</b> value used to identify the asynchronous I/O operation. The control point must use this handle while ending or cancelling the operation via <a href="https://msdn.microsoft.com/A0C0D01C-3A05-4498-9235-CBBF7D5D558F">EndSubscribeToEvents</a> or <a href="https://msdn.microsoft.com/FBEC2DF3-6D45-49F2-AAA8-6DED697BC5A6">CancelAsyncOperation</a>.


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
Failed to initiate the asynchronous operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="https://msdn.microsoft.com/4b18a5d4-f6e8-4670-93dd-ecd012940000">Device Error Codes</a>.</div>
<div> </div>



## -remarks



Event subscription should be completed before querying any evented state variables with <a href="https://msdn.microsoft.com/1E97589C-A06B-4012-A2A2-C88BBE9B2530">BeginQueryStateVariable</a>. If this does not occur,  <b>UPNP_E_VARIABLE_VALUE_UNKNOWN</b> is returned, and  event subscription will take place internally. As a result, the next <b>BeginQueryStateVariable</b> call will succeed.

<div class="alert"><b>Note</b>  For services without evented variables, <a href="https://msdn.microsoft.com/1E97589C-A06B-4012-A2A2-C88BBE9B2530">BeginQueryStateVariable</a> will always behave as expected.</div>
<div> </div>
Calling this method multiple times will result in the addition of multiple callbacks.




## -see-also




<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>



<a href="https://msdn.microsoft.com/FBEC2DF3-6D45-49F2-AAA8-6DED697BC5A6">IUPnPServiceAsync::CancelAsyncOperation</a>



<a href="https://msdn.microsoft.com/A0C0D01C-3A05-4498-9235-CBBF7D5D558F">IUPnPServiceAsync::EndSubscribeToEvents</a>
 

 

