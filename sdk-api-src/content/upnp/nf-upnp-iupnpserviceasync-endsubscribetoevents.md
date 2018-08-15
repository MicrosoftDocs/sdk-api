---
UID: NF:upnp.IUPnPServiceAsync.EndSubscribeToEvents
title: IUPnPServiceAsync::EndSubscribeToEvents
author: windows-sdk-content
description: EndSubscribeToEvents method retrieves the results of a previous BeginSubscribeToEvents operation.
old-location: upnp\iupnpserviceasync_endsubscribetoevents.htm
old-project: upnp
ms.assetid: A0C0D01C-3A05-4498-9235-CBBF7D5D558F
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: EndSubscribeToEvents, EndSubscribeToEvents method [UPnP APIs], EndSubscribeToEvents method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],EndSubscribeToEvents method, IUPnPServiceAsync.EndSubscribeToEvents, IUPnPServiceAsync::EndSubscribeToEvents, upnp.iupnpserviceasync_endsubscribetoevents, upnp/IUPnPServiceAsync::EndSubscribeToEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.redist: 
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
 - IUPnPServiceAsync.EndSubscribeToEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPServiceAsync::EndSubscribeToEvents


## -description


The <b>EndSubscribeToEvents</b> method retrieves the results of  a previous  <a href="https://msdn.microsoft.com/605629CB-9DBA-4130-B55D-957187551435">BeginSubscribeToEvents</a> operation.


## -parameters




### -param ullRequestID [in]

A 64-bit <b>ULONG</b> value that corresponds to the <a href="https://msdn.microsoft.com/605629CB-9DBA-4130-B55D-957187551435">BeginSubscribeToEvents</a> operation requested prior to this call.


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
The remote operation failed due to an HTTP problem. To retrieve the HTTP error code, use <a href="https://msdn.microsoft.com/8593b800-ae0a-41b8-9a61-92bdfc106c8b">IUPnPService::LastTransportStatus</a>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Some values can indicate that an error was received from a UPnP-certified device. For more information, see <a href="https://msdn.microsoft.com/4b18a5d4-f6e8-4670-93dd-ecd012940000">Device Error Codes</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/605629CB-9DBA-4130-B55D-957187551435">BeginSubscribeToEvents</a>



<a href="https://msdn.microsoft.com/8593b800-ae0a-41b8-9a61-92bdfc106c8b">IUPnPService::LastTransportStatus</a>



<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>
 

 

