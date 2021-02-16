---
UID: NC:rtmv2._EVENT_CALLBACK
title: _EVENT_CALLBACK (rtmv2.h)
description: The RTM_EVENT_CALLBACK callback is used by the routing table manager to inform a client that the specified event occurred.
helpviewer_keywords: ["RTM_CHANGE_NOTIFICATION","RTM_ENTITY_DEREGISTERED","RTM_ENTITY_REGISTERED","RTM_EVENT_CALLBACK","RTM_EVENT_CALLBACK callback function [RAS]","RTM_EVENT_CALLBACK callback function pointer [RAS]","RTM_ROUTE_EXPIRED","_EVENT_CALLBACK","_EVENT_CALLBACK callback","_rtmv2ref_rtm_event_callback","rras.rtm_event_callback","rtmv2/RTM_EVENT_CALLBACK"]
old-location: rras\rtm_event_callback.htm
tech.root: RRAS
ms.assetid: 57179cea-d92b-4199-bb61-b34d980532cf
ms.date: 12/05/2018
ms.keywords: RTM_CHANGE_NOTIFICATION, RTM_ENTITY_DEREGISTERED, RTM_ENTITY_REGISTERED, RTM_EVENT_CALLBACK, RTM_EVENT_CALLBACK callback function [RAS], RTM_EVENT_CALLBACK callback function pointer [RAS], RTM_ROUTE_EXPIRED, _EVENT_CALLBACK, _EVENT_CALLBACK callback, _rtmv2ref_rtm_event_callback, rras.rtm_event_callback, rtmv2/RTM_EVENT_CALLBACK
req.header: rtmv2.h
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
 - _EVENT_CALLBACK
 - rtmv2/_EVENT_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Rtmv2.h
api_name:
 - RTM_EVENT_CALLBACK
---

# _EVENT_CALLBACK callback function


## -description

The 
<b>RTM_EVENT_CALLBACK</b> callback is used by the routing table manager to inform a client that the specified event occurred.

## -parameters

### -param RtmRegHandle

Handle to the client to which the routing table manager is sending the notification.

### -param EventType

Specifies the event about which the routing table manager is notifying the client. The following values are used. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_ENTITY_REGISTERED"></a><a id="rtm_entity_registered"></a><dl>
<dt><b>RTM_ENTITY_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
A client has just registered with the routing table manager.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ENTITY_DEREGISTERED"></a><a id="rtm_entity_deregistered"></a><dl>
<dt><b>RTM_ENTITY_DEREGISTERED</b></dt>
</dl>
</td>
<td width="60%">
A client has just unregistered.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ROUTE_EXPIRED"></a><a id="rtm_route_expired"></a><dl>
<dt><b>RTM_ROUTE_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
A route has timed out.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_CHANGE_NOTIFICATION"></a><a id="rtm_change_notification"></a><dl>
<dt><b>RTM_CHANGE_NOTIFICATION</b></dt>
</dl>
</td>
<td width="60%">
A change notification has been made.

</td>
</tr>
</table>

### -param Context1

For RTM_ENTITY_REGISTERED calls: Contains the handle to the entity that registered. 




For RTM_ENTITY_DEREGISTERED calls: Contains the handle to the entity that unregistered.

For RTM_ROUTE_EXPIRED calls: Contains the handle to the route that timed out.

For RTM_CHANGE_NOTIFICATION calls: Contains the handle to the change notification.

### -param Context2

For RTM_ENTITY_REGISTERED calls: Contains a pointer to the 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_info">RTM_ENTITY_INFO</a> structure referred to by the handle in <i>Context1</i>. If the client must retain this information, the client must copy it to a structure it has allocated. 




For RTM_ENTITY_DEREGISTERED calls: Contains a pointer to the 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_info">RTM_ENTITY_INFO</a> structure referred to by the handle in <i>Context1</i>. If the client must retain this information, the client must copy it to a structure it has allocated.

For RTM_ROUTE_EXPIRED calls: Contains a pointer to the 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a> structure referred to by the handle in <i>Context1</i>. If the client must retain this information, the client must copy it to a structure it has allocated.

For RTM_CHANGE_NOTIFICATION calls: Contains the notification context that was given to the client by a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a>.

## -returns

If the routing table manager issues an RTM_ROUTE_EXPIRED callback, and the client returns to the routing table manager the value ERROR_NOT_SUPPORTED, the routing table manager will delete the route from the routing table.

All other errors returned by the client are ignored.

## -remarks

After a client has registered for change notification, the routing table manager uses this callback to keep the client informed about events.

If a client receives an 
<b>RTM_EVENT_CALLBACK</b> for the RTM_ENTITY_REGISTERED or RTM_ENTITY_DEREGISTERED events, the client must not make calls to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>, 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmderegisterentity">RtmDeregisterEntity</a>, or 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetregisteredentities">RtmGetRegisteredEntities</a> in the context of this callback.

If a client receives an 
<b>RTM_EVENT_CALLBACK</b> for the RTM_CHANGE_NOTIFICATION event, the client must not call 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterforchangenotification">RtmRegisterForChangeNotification</a> in the context of this callback.

## -see-also

<a href="/windows/desktop/api/rtmv2/ne-rtmv2-rtm_event_type">RTM_EVENT_TYPE</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>