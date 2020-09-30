---
UID: NF:upnp.IUPnPServiceAsync.EndQueryStateVariable
title: IUPnPServiceAsync::EndQueryStateVariable (upnp.h)
description: EndQueryStateVariable method retrieves the results of a previous BeginQueryStateVariable operation and retrieves the resultant service-specific state variable value.
helpviewer_keywords: ["EndQueryStateVariable","EndQueryStateVariable method [UPnP APIs]","EndQueryStateVariable method [UPnP APIs]","IUPnPServiceAsync interface","IUPnPServiceAsync interface [UPnP APIs]","EndQueryStateVariable method","IUPnPServiceAsync.EndQueryStateVariable","IUPnPServiceAsync::EndQueryStateVariable","upnp.iupnpserviceasync_endquerystatevariable","upnp/IUPnPServiceAsync::EndQueryStateVariable"]
old-location: upnp\iupnpserviceasync_endquerystatevariable.htm
tech.root: upnp
ms.assetid: 82AAB2C4-46A9-4545-95E1-887841735815
ms.date: 12/05/2018
ms.keywords: EndQueryStateVariable, EndQueryStateVariable method [UPnP APIs], EndQueryStateVariable method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],EndQueryStateVariable method, IUPnPServiceAsync.EndQueryStateVariable, IUPnPServiceAsync::EndQueryStateVariable, upnp.iupnpserviceasync_endquerystatevariable, upnp/IUPnPServiceAsync::EndQueryStateVariable
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
 - IUPnPServiceAsync::EndQueryStateVariable
 - upnp/IUPnPServiceAsync::EndQueryStateVariable
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
 - IUPnPServiceAsync.EndQueryStateVariable
---

# IUPnPServiceAsync::EndQueryStateVariable


## -description

The <b>EndQueryStateVariable</b> method retrieves the results of  a previous  <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginquerystatevariable">BeginQueryStateVariable</a> operation and retrieves the resultant service-specific state variable value.

## -parameters

### -param ullRequestID [in]

Pointer to a 64-bit <b>ULONG</b> value that corresponds to the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginquerystatevariable">BeginQueryStateVariable</a> operation initiated prior to this call.

### -param pValue [out, retval]

On input, contains an empty array. On output,  receives a reference to the value of the variable specified in <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginquerystatevariable">BeginQueryStateVariable</a> by <i>bstrVariableName</i>. The type of the data returned depends on the state variable for which the query was invoked.

<div class="alert"><b>Note</b>  Clear this parameter with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a>.</div>
<div> </div>

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
<dt><b>UPNP_E_DEVICE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The state variable is not evented and the remote query returned an error code. This is not a transport error; the device received the request, but it returned an error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_VARIABLE</b></dt>
</dl>
</td>
<td width="60%">
The requested state variable does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DEVICE_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The device has not responded within the 30 second time-out period.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_ARGUMENTS</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments passed with <i>vInActionArgs</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_PROTOCOL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The query did not complete because of problems at the UPnP protocol level.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_TRANSPORT_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The state variable is not evented and the remote query for the value failed because of an HTTP problem. To retrieve the HTTP error code, use <a href="/windows/desktop/api/upnp/nf-upnp-iupnpservice-get_lasttransportstatus">IUPnPService::LastTransportStatus</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_VARIABLE_VALUE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The state variable is evented, but the UPnP software cannot return a value because it is still waiting for an event notification.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="/windows/desktop/UPnP/device-error-codes">Device Error Codes</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpservice-get_lasttransportstatus">IUPnPService::LastTransportStatus</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-endquerystatevariable">IUPnPServiceAsync::EndQueryStateVariable</a>