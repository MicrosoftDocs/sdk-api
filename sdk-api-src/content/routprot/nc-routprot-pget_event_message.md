---
UID: NC:routprot.PGET_EVENT_MESSAGE
title: PGET_EVENT_MESSAGE
author: windows-driver-content
description: The GetEventMessage function gets an entry from the routing protocol's message queue. The routing protocol uses the queue to inform the router manager of asynchronous events.
old-location: rras\geteventmessage.htm
old-project: RRAS
ms.assetid: 59aa7bd8-3510-4ca0-90f1-2667dcb4abf0
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: GetEventMessage, GetEventMessage callback function [RAS], PGET_EVENT_MESSAGE, PGET_EVENT_MESSAGE callback, ROUTER_STOPPED, SAVE_GLOBAL_CONFIG_INFO, SAVE_INTERFACE_CONFIG_INFO, UPDATE_COMPLETE, _mpr_geteventmessage, routprot/GetEventMessage, rras.geteventmessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Routprot.h
api_name:
-	GetEventMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PGET_EVENT_MESSAGE callback function


## -description


The 
<b>GetEventMessage</b> function gets an entry from the routing protocol's message queue. The routing protocol uses the queue to inform the router manager of asynchronous events.


## -parameters




### -param *Event [out]

Pointer to an event. Information about this event is reported in the associated message. Note that this is not an event object. (The <b>ROUTING_PROTOCOL_EVENTS</b> type is declared in Routprot.h.) 




This parameter receives one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ROUTER_STOPPED"></a><a id="router_stopped"></a><dl>
<dt><b>ROUTER_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The router protocol shut down successfully. The message is empty for this event. (See 
<a href="https://msdn.microsoft.com/8b9459f8-152c-4ec1-9ed0-2b27a56f521d">StopProtocol</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="SAVE_GLOBAL_CONFIG_INFO"></a><a id="save_global_config_info"></a><dl>
<dt><b>SAVE_GLOBAL_CONFIG_INFO</b></dt>
</dl>
</td>
<td width="60%">
The routing protocol reports that its global configuration information has been changed by an external agent, that is, through means other than 
<a href="https://msdn.microsoft.com/fd977a71-bfa7-40e4-9afc-4824989f857f">SetGlobalInfo</a>. The routing protocol requests that the router manager retrieve and permanently store this information. The message is empty for this event.

</td>
</tr>
<tr>
<td width="40%"><a id="SAVE_INTERFACE_CONFIG_INFO"></a><a id="save_interface_config_info"></a><dl>
<dt><b>SAVE_INTERFACE_CONFIG_INFO</b></dt>
</dl>
</td>
<td width="60%">
The routing protocol reports that the configuration information associated with one of its interfaces has been changed by an external agent, that is, through means other than 
<a href="https://msdn.microsoft.com/abcfa220-a860-48cc-92c5-60ce655678b7">SetInterfaceInfo</a>. The routing protocol requests that the router manager retrieve and permanently store this information. The message contains the ID of the interface.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDATE_COMPLETE"></a><a id="update_complete"></a><dl>
<dt><b>UPDATE_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The routing protocol has completed an autostatic update request from the router manager. The router manager converts received routing information to static. The message contains the index of the interface on which the update was performed, the type of the information received (routes or services), and the result field, which indicates whether the update succeeded. See 
<a href="https://msdn.microsoft.com/5942c856-f504-4e2d-86c8-f3207c787ed5">DoUpdateRoutes</a> and 
<a href="https://msdn.microsoft.com/1e7b5e3c-0d90-445e-93a3-57ee08d19ec2">DoUpdateServices</a>.

</td>
</tr>
</table>
 


### -param *Result [out]

Pointer to a 
<a href="https://msdn.microsoft.com/94f3069f-c282-4dea-84f9-48645f4e1593">MESSAGE</a> union. The contents of the message are specific to the reported event. 




This parameter is optional; the caller may specify <b>NULL</b> for this parameter.


## -returns



If the entry is retrieved successfully, the return value is NO_ERROR.

If the routing protocol's message queue does not contain any entries, the return value is ERROR_NO_MORE_ITEMS.




## -see-also




<a href="https://msdn.microsoft.com/5942c856-f504-4e2d-86c8-f3207c787ed5">DoUpdateRoutes</a>



<a href="https://msdn.microsoft.com/1e7b5e3c-0d90-445e-93a3-57ee08d19ec2">DoUpdateServices</a>



<a href="https://msdn.microsoft.com/94f3069f-c282-4dea-84f9-48645f4e1593">MESSAGE</a>



<a href="https://msdn.microsoft.com/fd780458-ef23-4ef2-8fe8-29b32100917f">Routing Protocol Interface Functions</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>



<a href="https://msdn.microsoft.com/fd977a71-bfa7-40e4-9afc-4824989f857f">SetGlobalInfo</a>



<a href="https://msdn.microsoft.com/abcfa220-a860-48cc-92c5-60ce655678b7">SetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/8b9459f8-152c-4ec1-9ed0-2b27a56f521d">StopProtocol</a>
 

 

