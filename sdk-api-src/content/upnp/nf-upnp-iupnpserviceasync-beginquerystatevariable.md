---
UID: NF:upnp.IUPnPServiceAsync.BeginQueryStateVariable
title: IUPnPServiceAsync::BeginQueryStateVariable (upnp.h)
description: BeginQueryStateVariable method initiates an asynchronous request for the state variable value from a specific service.
helpviewer_keywords: ["BeginQueryStateVariable","BeginQueryStateVariable method [UPnP APIs]","BeginQueryStateVariable method [UPnP APIs]","IUPnPServiceAsync interface","IUPnPServiceAsync interface [UPnP APIs]","BeginQueryStateVariable method","IUPnPServiceAsync.BeginQueryStateVariable","IUPnPServiceAsync::BeginQueryStateVariable","upnp.iupnpserviceasync_beginquerystatevariable","upnp/IUPnPServiceAsync::BeginQueryStateVariable"]
old-location: upnp\iupnpserviceasync_beginquerystatevariable.htm
tech.root: upnp
ms.assetid: 1E97589C-A06B-4012-A2A2-C88BBE9B2530
ms.date: 12/05/2018
ms.keywords: BeginQueryStateVariable, BeginQueryStateVariable method [UPnP APIs], BeginQueryStateVariable method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],BeginQueryStateVariable method, IUPnPServiceAsync.BeginQueryStateVariable, IUPnPServiceAsync::BeginQueryStateVariable, upnp.iupnpserviceasync_beginquerystatevariable, upnp/IUPnPServiceAsync::BeginQueryStateVariable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPServiceAsync::BeginQueryStateVariable
 - upnp/IUPnPServiceAsync::BeginQueryStateVariable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceAsync.BeginQueryStateVariable
---

# IUPnPServiceAsync::BeginQueryStateVariable


## -description

The <b>BeginQueryStateVariable</b> method initiates an asynchronous request for the state variable value from a specific service. Additionally, if opt-in is indicated for a delayed Service Control Protocol Description (SCPD) download and event subscription, and it has not taken place already, this method will initiate SCPD download and event subscription.

## -parameters

### -param bstrVariableName [in]

Specifies the requested state variable value.

### -param pAsyncResult [in, optional]

Pointer  to a <a href="/windows/desktop/api/upnp/nn-upnp-iupnpasyncresult">IUPnPAsyncResult</a> object. When the <b>BeginQueryStateVariable</b> call is complete, 
	UPnP will use the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpasyncresult-asyncoperationcomplete">IUPnPAsyncResult::AsyncOperationComplete</a> method to notify the control 
	point.

### -param pullRequestID [out]

Pointer to a 64-bit <b>ULONG</b> value used to identify the asynchronous I/O operation. The UPnP control point must use this handle when ending or cancelling this  operation with <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-endquerystatevariable">EndQueryStateVariable</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_VARIABLE</b></dt>
</dl>
</td>
<td width="60%">
The requested state variable, indicated by <i>bstrVariableName</i>, does not exist.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="/windows/desktop/UPnP/device-error-codes">Device Error Codes</a>.</div>
<div> </div>

## -remarks

Event subscription should be completed before querying any evented state variables with this method. If this does not occur,  <b>UPNP_E_VARIABLE_VALUE_UNKNOWN</b> is returned, and  event subscription will take place internally. As a result, the next <b>BeginQueryStateVariable</b> call will succeed.

<div class="alert"><b>Note</b>  For services without evented variables, this method will always behave as expected.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-cancelasyncoperation">IUPnPServiceAsync::CancelAsyncOperation</a>