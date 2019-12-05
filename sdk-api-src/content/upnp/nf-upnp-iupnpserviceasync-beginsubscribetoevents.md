---
UID: NF:upnp.IUPnPServiceAsync.BeginSubscribeToEvents
title: IUPnPServiceAsync::BeginSubscribeToEvents (upnp.h)
description: BeginSubscribeToEvents initiates event subscription in asynchronous mode and registers the application callback with the UPnP framework.
old-location: upnp\iupnpserviceasync_beginsubscribetoevents.htm
tech.root: upnp
ms.assetid: 605629CB-9DBA-4130-B55D-957187551435
ms.date: 12/05/2018
ms.keywords: BeginSubscribeToEvents, BeginSubscribeToEvents method [UPnP APIs], BeginSubscribeToEvents method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],BeginSubscribeToEvents method, IUPnPServiceAsync.BeginSubscribeToEvents, IUPnPServiceAsync::BeginSubscribeToEvents, upnp.iupnpserviceasync_beginsubscribetoevents, upnp/IUPnPServiceAsync::BeginSubscribeToEvents
ms.topic: method
f1_keywords:
- upnp/IUPnPServiceAsync.BeginSubscribeToEvents
dev_langs:
- c++
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
req.lib: 
req.dll: Upnp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Upnp.dll
api_name:
- IUPnPServiceAsync.BeginSubscribeToEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPServiceAsync::BeginSubscribeToEvents


## -description


The <b>BeginSubscribeToEvents</b> initiates event subscription in asynchronous mode and  registers the application callback with the UPnP framework.


## -parameters




### -param pUnkCallback [in]

Specifies the reference to the interface object that contains the callback to register. This object must either support the <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpservicecallback">IUPnPServiceCallback</a> interface or the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface.


### -param pAsyncResult [in, optional]

Specifies a reference to <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpasyncresult">IUPnPAsyncResult</a> object. When the <b>BeginSubscribeToEvents</b> call is complete, 
	UPnP will use the <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpasyncresult-asyncoperationcomplete">IUPnPAsyncResult::AsyncOperationComplete</a> method to notify the control point.



### -param pullRequestID [out]

Pointer to a 64-bit <b>ULONG</b> value used to identify the asynchronous I/O operation. The control point must use this handle while ending or cancelling the operation via <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-endsubscribetoevents">EndSubscribeToEvents</a> or <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-cancelasyncoperation">CancelAsyncOperation</a>.


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
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="https://docs.microsoft.com/windows/desktop/UPnP/device-error-codes">Device Error Codes</a>.</div>
<div> </div>



## -remarks



Event subscription should be completed before querying any evented state variables with <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginquerystatevariable">BeginQueryStateVariable</a>. If this does not occur,  <b>UPNP_E_VARIABLE_VALUE_UNKNOWN</b> is returned, and  event subscription will take place internally. As a result, the next <b>BeginQueryStateVariable</b> call will succeed.

<div class="alert"><b>Note</b>  For services without evented variables, <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginquerystatevariable">BeginQueryStateVariable</a> will always behave as expected.</div>
<div> </div>
Calling this method multiple times will result in the addition of multiple callbacks.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>



<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-cancelasyncoperation">IUPnPServiceAsync::CancelAsyncOperation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-endsubscribetoevents">IUPnPServiceAsync::EndSubscribeToEvents</a>
 

 

