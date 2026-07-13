---
UID: NC:traffic.TCI_NOTIFY_HANDLER
title: TCI_NOTIFY_HANDLER (traffic.h)
description: The ClNotifyHandler function is used by traffic control to notify the client of various traffic control specific events, including the deletion of flows, changes in filter parameters, or the closing of an interface.
helpviewer_keywords: ["ClNotifyHandler","ClNotifyHandler callback","ClNotifyHandler callback function [QOS]","TCI_NOTIFY_HANDLER","TCI_NOTIFY_HANDLER callback function [QOS]","_gqos_clnotifyhandler","qos.clnotifyhandler","traffic/ClNotifyHandler"]
old-location: qos\clnotifyhandler.htm
tech.root: QOS
ms.assetid: cacf4c21-d831-462c-b9e8-fd51fcf8e4e4
ms.date: 12/05/2018
ms.keywords: ClNotifyHandler, ClNotifyHandler callback, ClNotifyHandler callback function [QOS], TCI_NOTIFY_HANDLER, TCI_NOTIFY_HANDLER callback function [QOS], _gqos_clnotifyhandler, qos.clnotifyhandler, traffic/ClNotifyHandler
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
 - TCI_NOTIFY_HANDLER
 - traffic/TCI_NOTIFY_HANDLER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Traffic.h
api_name:
 - TCI_NOTIFY_HANDLER
---

# TCI_NOTIFY_HANDLER callback function


## -description

The 
<i>ClNotifyHandler</i> function is used by traffic control to notify the client of various traffic control–specific events, including the deletion of flows, changes in filter parameters, or the closing of an interface.

The 
<i>ClNotifyHandler</i> callback function should be exposed by all clients using traffic control services.

## -parameters

### -param ClRegCtx [in]

Client registration context, provided to traffic control by the client with the client's call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcregisterclient">TcRegisterClient</a> function.

### -param ClIfcCtx [in]

Client interface context, provided to traffic control by the client with the client's call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcopeninterfacea">TcOpenInterface</a> function. Note that during a TC_NOTIFY_IFC_UP event, <i>ClIfcCtx</i> is not available and will be set to <b>NULL</b>.

### -param Event [in]

Describes the notification event. See the Remarks section for a list of notification events.

### -param SubCode [in]

Handle used to further qualify a notification event. See Note below for 64-bit for Windows programming issues.

### -param BufSize [in]

Size of the buffer included with the notification event, in bytes.

### -param Buffer [in]

Buffer containing the detailed event information associated with <i>Event</i> and <i>SubCode</i>.

## -remarks

Notification events may require the traffic control client to take particular action or respond appropriately, for example, removing filters or enumerating flows for affected interfaces.

The following table describes the various notification events.

<table>
<tr>
<th>Event</th>
<th>SubCode</th>
<th>Buffer contents</th>
<th>Remarks</th>
</tr>
<tr>
<td>TC_NOTIFY_IFC_UP</td>
<td>None</td>
<td>Interface name of the new interface</td>
<td>A new traffic control interface is coming up, and the list of addresses is indicated.</td>
</tr>
<tr>
<td>TC_NOTIFY_IFC_CLOSE</td>
<td>Reason for close</td>
<td>Interface name of the closed interface</td>
<td>Indicates an interface that was opened by the client is being closed by the system. Note that the interface and its supported flows and filters are closed by the system upon return from the notification handler. The client does not need to close the interface, delete flows, or delete filters.</td>
</tr>
<tr>
<td>TC_NOTIFY_IFC_CHANGE</td>
<td>None</td>
<td>New parameter value</td>
<td>Used to notify clients that have registered for interface change notification through the <i>NotifyChange</i> parameter of the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcqueryinterface">TcQueryInterface</a> function.</td>
</tr>
<tr>
<td>TC_NOTIFY_PARAM_CHANGED</td>
<td>Pointer to the GUID for a traffic control parameter queried using the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcqueryinterface">TcQueryInterface</a> function.</td>
<td>New parameter value</td>
<td>This event is notified as a result of a change in a parameter previously queried with the <i>NotifyChange</i> flag set.</td>
</tr>
<tr>
<td>TC_NOTIFY_FLOW_CLOSE</td>
<td><i>ClFlowCtx</i></td>
<td></td>
<td>Indicates system closure of a client-created flow. The system deletes all associated filters.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Use of the 
<i>ClNotifyHandler</i> function requires administrative privilege.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcopeninterfacea">TcOpenInterface</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcqueryinterface">TcQueryInterface</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcregisterclient">TcRegisterClient</a>
