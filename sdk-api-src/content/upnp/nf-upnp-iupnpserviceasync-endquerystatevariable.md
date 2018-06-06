---
UID: NF:upnp.IUPnPServiceAsync.EndQueryStateVariable
title: IUPnPServiceAsync::EndQueryStateVariable
author: windows-sdk-content
description: EndQueryStateVariable method retrieves the results of a previous BeginQueryStateVariable operation and retrieves the resultant service-specific state variable value.
old-location: upnp\iupnpserviceasync_endquerystatevariable.htm
old-project: UPnP
ms.assetid: 82AAB2C4-46A9-4545-95E1-887841735815
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: EndQueryStateVariable, EndQueryStateVariable method [UPnP APIs], EndQueryStateVariable method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],EndQueryStateVariable method, IUPnPServiceAsync.EndQueryStateVariable, IUPnPServiceAsync::EndQueryStateVariable, upnp.iupnpserviceasync_endquerystatevariable, upnp/IUPnPServiceAsync::EndQueryStateVariable
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceAsync.EndQueryStateVariable
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPServiceAsync::EndQueryStateVariable


## -description


The <b>EndQueryStateVariable</b> method retrieves the results of  a previous  <a href="https://msdn.microsoft.com/1E97589C-A06B-4012-A2A2-C88BBE9B2530">BeginQueryStateVariable</a> operation and retrieves the resultant service-specific state variable value.



## -parameters




### -param ullRequestID [in]

Pointer to a 64-bit <b>ULONG</b> value that corresponds to the <a href="https://msdn.microsoft.com/1E97589C-A06B-4012-A2A2-C88BBE9B2530">BeginQueryStateVariable</a> operation initiated prior to this call.


### -param pValue [out, retval]

On input, contains an empty array. On output,  receives a reference to the value of the variable specified in <a href="https://msdn.microsoft.com/1E97589C-A06B-4012-A2A2-C88BBE9B2530">BeginQueryStateVariable</a> by <i>bstrVariableName</i>. The type of the data returned depends on the state variable for which the query was invoked.

<div class="alert"><b>Note</b>  Clear this parameter with <a href="https://msdn.microsoft.com/28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a>.</div>
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
The state variable is not evented and the remote query for the value failed because of an HTTP problem. To retrieve the HTTP error code, use <a href="https://msdn.microsoft.com/8593b800-ae0a-41b8-9a61-92bdfc106c8b">IUPnPService::LastTransportStatus</a>.

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
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="https://msdn.microsoft.com/4b18a5d4-f6e8-4670-93dd-ecd012940000">Device Error Codes</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8593b800-ae0a-41b8-9a61-92bdfc106c8b">IUPnPService::LastTransportStatus</a>



<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>



<a href="https://msdn.microsoft.com/82AAB2C4-46A9-4545-95E1-887841735815">IUPnPServiceAsync::EndQueryStateVariable</a>
 

 

