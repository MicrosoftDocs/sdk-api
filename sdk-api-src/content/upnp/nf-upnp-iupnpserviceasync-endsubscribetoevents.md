---
UID: NF:upnp.IUPnPServiceAsync.EndSubscribeToEvents
title: IUPnPServiceAsync::EndSubscribeToEvents (upnp.h)
description: EndSubscribeToEvents method retrieves the results of a previous BeginSubscribeToEvents operation.
helpviewer_keywords: ["EndSubscribeToEvents","EndSubscribeToEvents method [UPnP APIs]","EndSubscribeToEvents method [UPnP APIs]","IUPnPServiceAsync interface","IUPnPServiceAsync interface [UPnP APIs]","EndSubscribeToEvents method","IUPnPServiceAsync.EndSubscribeToEvents","IUPnPServiceAsync::EndSubscribeToEvents","upnp.iupnpserviceasync_endsubscribetoevents","upnp/IUPnPServiceAsync::EndSubscribeToEvents"]
old-location: upnp\iupnpserviceasync_endsubscribetoevents.htm
tech.root: upnp
ms.assetid: A0C0D01C-3A05-4498-9235-CBBF7D5D558F
ms.date: 12/05/2018
ms.keywords: EndSubscribeToEvents, EndSubscribeToEvents method [UPnP APIs], EndSubscribeToEvents method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],EndSubscribeToEvents method, IUPnPServiceAsync.EndSubscribeToEvents, IUPnPServiceAsync::EndSubscribeToEvents, upnp.iupnpserviceasync_endsubscribetoevents, upnp/IUPnPServiceAsync::EndSubscribeToEvents
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
 - IUPnPServiceAsync::EndSubscribeToEvents
 - upnp/IUPnPServiceAsync::EndSubscribeToEvents
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
 - IUPnPServiceAsync.EndSubscribeToEvents
---

# IUPnPServiceAsync::EndSubscribeToEvents


## -description

The <b>EndSubscribeToEvents</b> method retrieves the results of  a previous  <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginsubscribetoevents">BeginSubscribeToEvents</a> operation.

## -parameters

### -param ullRequestID [in]

A 64-bit <b>ULONG</b> value that corresponds to the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginsubscribetoevents">BeginSubscribeToEvents</a> operation requested prior to this call.

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
The device received the request, but returned an error.

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
<dt><b>UPNP_E_PROTOCOL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The query did not complete due to problems at the UPnP protocol level.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_TRANSPORT_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The remote operation failed due to an HTTP problem. To retrieve the HTTP error code, use <a href="/windows/desktop/api/upnp/nf-upnp-iupnpservice-get_lasttransportstatus">IUPnPService::LastTransportStatus</a>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="/windows/desktop/UPnP/device-error-codes">Device Error Codes</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginsubscribetoevents">BeginSubscribeToEvents</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpservice-get_lasttransportstatus">IUPnPService::LastTransportStatus</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>