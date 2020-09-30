---
UID: NF:upnp.IUPnPServiceAsync.EndInvokeAction
title: IUPnPServiceAsync::EndInvokeAction (upnp.h)
description: EndInvokeAction method retrieves the results of a previous BeginInvokeAction operation and retrieves the resultant output arguments.
helpviewer_keywords: ["EndInvokeAction","EndInvokeAction method [UPnP APIs]","EndInvokeAction method [UPnP APIs]","IUPnPServiceAsync interface","IUPnPServiceAsync interface [UPnP APIs]","EndInvokeAction method","IUPnPServiceAsync.EndInvokeAction","IUPnPServiceAsync::EndInvokeAction","upnp.iupnpserviceasync_endinvokeaction","upnp/IUPnPServiceAsync::EndInvokeAction"]
old-location: upnp\iupnpserviceasync_endinvokeaction.htm
tech.root: upnp
ms.assetid: 1B10F8E9-D3C9-432B-B773-77B4BB82224C
ms.date: 12/05/2018
ms.keywords: EndInvokeAction, EndInvokeAction method [UPnP APIs], EndInvokeAction method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],EndInvokeAction method, IUPnPServiceAsync.EndInvokeAction, IUPnPServiceAsync::EndInvokeAction, upnp.iupnpserviceasync_endinvokeaction, upnp/IUPnPServiceAsync::EndInvokeAction
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
 - IUPnPServiceAsync::EndInvokeAction
 - upnp/IUPnPServiceAsync::EndInvokeAction
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
 - IUPnPServiceAsync.EndInvokeAction
---

# IUPnPServiceAsync::EndInvokeAction


## -description

The <b>EndInvokeAction</b> method retrieves the results of  a previous <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-begininvokeaction">BeginInvokeAction</a> operation and retrieves the resultant output arguments.

## -parameters

### -param ullRequestID [in, out]

On input, contains a reference to an empty array. On output, receives a reference to the array of service-specific output arguments. In the event the action doesn't have output arguments, this parameter contains an empty array.

<div class="alert"><b>Note</b>  Clear this parameter with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a>.</div>
<div> </div>

### -param pvOutActionArgs [in, out]

On input contains a reference to an empty array. On output, receives a reference to a VARIANT that contains the return value of the invoked action. 

<div class="alert"><b>Note</b>  Clear this parameter with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a>.</div>
<div> </div>

### -param pvRetVal [in]

A 64-bit <b>ULONG</b> value that corresponds to the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-begininvokeaction">BeginInvokeAction</a> operation initiated prior to this call.

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
<dt><b>UPNP_E_DEVICE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_ARGUMENTS</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments passed is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_ACTION</b></dt>
</dl>
</td>
<td width="60%">
This action is not supported by the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_ERROR_PROCESSING_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
The device has sent a response that cannot be processed; for example, the response was corrupted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_PROTOCOL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred at the UPnP control-protocol level.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_TRANSPORT_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An HTTP error occurred. Use the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpservice-get_lasttransportstatus">IUPnPService::LastTransportStatus</a> property to obtain the actual HTTP status code.  

<div class="alert"><b>Note</b>  This error code is also returned when the SOAP response exceeds 100 kilobytes.
</div>
<div> </div>
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="/windows/desktop/UPnP/device-error-codes">Device Error Codes</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpservice-get_lasttransportstatus">IUPnPService::LastTransportStatus</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-begininvokeaction">IUPnPServiceAsync::BeginInvokeAction</a>