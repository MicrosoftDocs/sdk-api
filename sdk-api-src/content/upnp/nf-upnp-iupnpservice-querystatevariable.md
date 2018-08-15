---
UID: NF:upnp.IUPnPService.QueryStateVariable
title: IUPnPService::QueryStateVariable
author: windows-sdk-content
description: The QueryStateVariable method returns the value of the specified service's state variable.
old-location: upnp\iupnpservice_querystatevariable.htm
old-project: upnp
ms.assetid: d92785a2-e04c-4968-b515-019205180915
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IUPnPService interface [UPnP APIs],QueryStateVariable method, IUPnPService.QueryStateVariable, IUPnPService::QueryStateVariable, QueryStateVariable, QueryStateVariable method [UPnP APIs], QueryStateVariable method [UPnP APIs],IUPnPService interface, _upnp_iupnpservice_querystatevariable, upnp.iupnpservice_querystatevariable, upnp/IUPnPService::QueryStateVariable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
 - IUPnPService.QueryStateVariable
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPService::QueryStateVariable


## -description


The 
<b>QueryStateVariable</b> method returns the value of the specified service's state variable.


## -parameters




### -param bstrVariableName [in]

Specifies the state variable for which to return a value.


### -param pValue






#### - pvarValue [out]

Receives a reference to the value of the variable specified by <i>bstrVariableName</i>. The type of the data returned depends on the state variable for which the query was invoked. 




To free this parameter, use <a href="28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a>.
						


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns either one of the COM error codes defined in WinError.h or one of the UPnP-specific return values listed in the following table. Some of these values indicate that an error was received from a UPnP-certified device. For more information, see <a href="https://msdn.microsoft.com/4b18a5d4-f6e8-4670-93dd-ecd012940000">Device Error Codes</a>.

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
The variable is not evented and the remote query returned an error code. This is not a transport error; the device received the request, but it returned an error.

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
<dt><b>UPNP_E_INVALID_VARIABLE</b></dt>
</dl>
</td>
<td width="60%">
The variable does not exist.

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
The variable is not evented and the remote query for the value failed because of an HTTP problem. To retrieve the HTTP error code, use 
<a href="https://msdn.microsoft.com/8593b800-ae0a-41b8-9a61-92bdfc106c8b">IUPnPService::LastTransportStatus</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_VARIABLE_VALUE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The variable is evented, but the UPnP software cannot return a value because it is still waiting for an event notification.

</td>
</tr>
</table>
 




## -remarks



The UPnP Forum discourages use of this method. If possible, use a service-specific action, if one has been provided.

This method retrieves the values of evented variables from the service object's local cache. The cache contains the value for each variable indicated in the last event notification. This method retrieves the values of non-evented variables by sending a remote query to the device.

If an application invokes this method for an evented state variable, between the time a service first initializes itself and the time it processes its first event, <b>UPNP_E_VARIABLE_VALUE_UNKNOWN</b> is returned.

If an application invokes this method for a service that does not use events, and the HTTP request fails, <b>UPNP_E_TRANSPORT_ERROR</b> is returned. To view the status, use 
<a href="https://msdn.microsoft.com/8593b800-ae0a-41b8-9a61-92bdfc106c8b">IUPnPService::LastTransportStatus</a>.

<div class="alert"><b>Note</b>  The time.tz variable can contain incorrect timezone information on the control point. For example, you can have a device and a control point running in the same timezone, -7.00. When the control point queries a time.tz variable for the current time, the device returns a datestructure with the timezone value set to -8.00 instead of -7.00.<p class="note">To work around this issue, use the dataTime.tz variable type instead time.tz on the control point.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a>



<a href="https://msdn.microsoft.com/8593b800-ae0a-41b8-9a61-92bdfc106c8b">IUPnPService::LastTransportStatus</a>
 

 

