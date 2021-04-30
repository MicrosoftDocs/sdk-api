---
UID: NC:routprot.PGET_EVENT_MESSAGE
title: PGET_EVENT_MESSAGE (routprot.h)
description: The GetEventMessage function gets an entry from the routing protocol's message queue. The routing protocol uses the queue to inform the router manager of asynchronous events.
helpviewer_keywords: ["GetEventMessage","PGET_EVENT_MESSAGE","PGET_EVENT_MESSAGE callback","PGET_EVENT_MESSAGE callback function [RAS]","ROUTER_STOPPED","SAVE_GLOBAL_CONFIG_INFO","SAVE_INTERFACE_CONFIG_INFO","UPDATE_COMPLETE","_mpr_geteventmessage","routprot/PGET_EVENT_MESSAGE","rras.geteventmessage"]
old-location: rras\geteventmessage.htm
tech.root: RRAS
ms.assetid: 59aa7bd8-3510-4ca0-90f1-2667dcb4abf0
ms.date: 12/05/2018
ms.keywords: GetEventMessage, PGET_EVENT_MESSAGE, PGET_EVENT_MESSAGE callback, PGET_EVENT_MESSAGE callback function [RAS], ROUTER_STOPPED, SAVE_GLOBAL_CONFIG_INFO, SAVE_INTERFACE_CONFIG_INFO, UPDATE_COMPLETE, _mpr_geteventmessage, routprot/PGET_EVENT_MESSAGE, rras.geteventmessage
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PGET_EVENT_MESSAGE
 - routprot/PGET_EVENT_MESSAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - PGET_EVENT_MESSAGE
---

# PGET_EVENT_MESSAGE callback function


## -description

The 
<b>GetEventMessage</b> function gets an entry from the routing protocol's message queue. The routing protocol uses the queue to inform the router manager of asynchronous events.

## -parameters

### -param Event [out]

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
<a href="/windows/desktop/api/routprot/nc-routprot-pstop_protocol">StopProtocol</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="SAVE_GLOBAL_CONFIG_INFO"></a><a id="save_global_config_info"></a><dl>
<dt><b>SAVE_GLOBAL_CONFIG_INFO</b></dt>
</dl>
</td>
<td width="60%">
The routing protocol reports that its global configuration information has been changed by an external agent, that is, through means other than 
<a href="/windows/desktop/api/routprot/nc-routprot-pset_global_info">SetGlobalInfo</a>. The routing protocol requests that the router manager retrieve and permanently store this information. The message is empty for this event.

</td>
</tr>
<tr>
<td width="40%"><a id="SAVE_INTERFACE_CONFIG_INFO"></a><a id="save_interface_config_info"></a><dl>
<dt><b>SAVE_INTERFACE_CONFIG_INFO</b></dt>
</dl>
</td>
<td width="60%">
The routing protocol reports that the configuration information associated with one of its interfaces has been changed by an external agent, that is, through means other than 
<a href="/windows/desktop/api/routprot/nc-routprot-pset_interface_info">SetInterfaceInfo</a>. The routing protocol requests that the router manager retrieve and permanently store this information. The message contains the ID of the interface.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDATE_COMPLETE"></a><a id="update_complete"></a><dl>
<dt><b>UPDATE_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The routing protocol has completed an autostatic update request from the router manager. The router manager converts received routing information to static. The message contains the index of the interface on which the update was performed, the type of the information received (routes or services), and the result field, which indicates whether the update succeeded. See 
<a href="/windows/desktop/api/routprot/nc-routprot-pdo_update_routes">DoUpdateRoutes</a> and 
<a href="/previous-versions/windows/desktop/legacy/aa374005(v=vs.85)">DoUpdateServices</a>.

</td>
</tr>
</table>

### -param Result [out]

Pointer to a 
<a href="/windows/desktop/api/routprot/ns-routprot-message">MESSAGE</a> union. The contents of the message are specific to the reported event. 




This parameter is optional; the caller may specify <b>NULL</b> for this parameter.

## -returns

If the entry is retrieved successfully, the return value is NO_ERROR.

If the routing protocol's message queue does not contain any entries, the return value is ERROR_NO_MORE_ITEMS.

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pdo_update_routes">DoUpdateRoutes</a>



<a href="/previous-versions/windows/desktop/legacy/aa374005(v=vs.85)">DoUpdateServices</a>



<a href="/windows/desktop/api/routprot/ns-routprot-message">MESSAGE</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-functions">Routing Protocol Interface Functions</a>



<a href="/windows/desktop/RRAS/routing-protocol-interface-reference">Routing Protocol Interface Reference</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pset_global_info">SetGlobalInfo</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pset_interface_info">SetInterfaceInfo</a>



<a href="/windows/desktop/api/routprot/nc-routprot-pstop_protocol">StopProtocol</a>
