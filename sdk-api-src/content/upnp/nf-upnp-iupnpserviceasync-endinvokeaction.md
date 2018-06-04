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

# IUPnPServiceAsync::EndInvokeAction


## -description


The <b>EndInvokeAction</b> method retrieves the results of  a previous <a href="https://msdn.microsoft.com/40900CE1-03EE-451A-84DE-5C496EB2D7E5">BeginInvokeAction</a> operation and retrieves the resultant output arguments.


## -parameters




### -param ullRequestID [in]

A 64-bit <b>ULONG</b> value that corresponds to the <a href="https://msdn.microsoft.com/40900CE1-03EE-451A-84DE-5C496EB2D7E5">BeginInvokeAction</a> operation initiated prior to this call.


### -param pvOutActionArgs




### -param pvRetVal [in, out]

On input contains a reference to an empty array. On output, receives a reference to a VARIANT that contains the return value of the invoked action. 

<div class="alert"><b>Note</b>  Clear this parameter with <a href="https://msdn.microsoft.com/28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a>.</div>
<div> </div>

#### - pvarOutActionArgs [in, out]

On input, contains a reference to an empty array. On output, receives a reference to the array of service-specific output arguments. In the event the action doesn't have output arguments, this parameter contains an empty array.

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
An HTTP error occurred. Use the <a href="https://msdn.microsoft.com/8593b800-ae0a-41b8-9a61-92bdfc106c8b">IUPnPService::LastTransportStatus</a> property to obtain the actual HTTP status code.  

<div class="alert"><b>Note</b>  This error code is also returned when the SOAP response exceeds 100 kilobytes.
</div>
<div> </div>
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="https://msdn.microsoft.com/4b18a5d4-f6e8-4670-93dd-ecd012940000">Device Error Codes</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8593b800-ae0a-41b8-9a61-92bdfc106c8b">IUPnPService::LastTransportStatus</a>



<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>



<a href="https://msdn.microsoft.com/40900CE1-03EE-451A-84DE-5C496EB2D7E5">IUPnPServiceAsync::BeginInvokeAction</a>
 

 

