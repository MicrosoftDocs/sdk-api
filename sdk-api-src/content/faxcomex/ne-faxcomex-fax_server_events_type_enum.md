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

# FAX_SERVER_EVENTS_TYPE_ENUM enumeration


## -description


The <b>FAX_SERVER_EVENTS_TYPE_ENUM</b> enumeration defines the types of events the fax service sends to client applications that are listening for events. The members of this enumeration are bit values and can be used in combination.


## -enum-fields




### -field fsetNONE

No events are sent.


### -field fsetIN_QUEUE

The client requests notifications about fax jobs in the incoming queue. When the status of an incoming fax job changes, the fax service issues a notification of this type.


### -field fsetOUT_QUEUE

The client requests notification about fax jobs in the outgoing queue. When the status of an outgoing fax job changes, the fax service issues a notification of this type.


### -field fsetCONFIG

The client requests notifications about changes to the fax server configuration. When the configuration data changes, the fax service issues a notification of this type.


### -field fsetACTIVITY

The client requests notifications about the fax server activity. When the activity status of the fax server changes, the fax service issues a notification of this type. 


### -field fsetQUEUE_STATE

The client requests notifications about changes in the status of the fax job queue. When the status of the queue changes, the fax service issues a notification.


### -field fsetIN_ARCHIVE

The client requests notifications about the addition or removal of fax messages from the incoming archive. When a message is removed from the archive, the fax service issues a notification. The notification includes the archive type (inbound) and the unique ID of the fax message.


### -field fsetOUT_ARCHIVE

The client requests notifications about the addition or removal of fax messages from the outgoing archive. When a message is removed from the archive, the fax service issues a notification. The notification includes the archive type (outbound) and the unique ID of the fax message.


### -field fsetFXSSVC_ENDED

The client requests notifications when the fax service stops executing.


### -field fsetDEVICE_STATUS

The client requests notifications when a device status changes.


### -field fsetINCOMING_CALL

The client requests notifications when there is an incoming call.


## -remarks



The following table lists the <a href="https://msdn.microsoft.com/e8192f70-b0aa-4055-b67b-ff95991b66f2">IFaxServerNotify</a> methods called by each member.

<table class="clsStd">
<tr>
<th>Name</th>
<th>
<a href="https://msdn.microsoft.com/e8192f70-b0aa-4055-b67b-ff95991b66f2">IFaxServerNotify</a> method called</th>
</tr>
<tr>
<td>
fsetNONE

</td>
<td>
None

</td>
</tr>
<tr>
<td>
fsetIN_QUEUE

</td>
<td>
<b>OnIncomingJobAdded</b>

<b>OnIncomingJobRemoved</b>

<b>OnIncomingJobChanged</b>

</td>
</tr>
<tr>
<td>
fsetOUT_QUEUE

</td>
<td>
<b>OnOutgoingJobAdded</b>

<b>OnOutgoingJobRemoved</b>

<b>OnOutgoingJobChanged</b>

</td>
</tr>
<tr>
<td>
fsetCONFIG

</td>
<td>
<b>OnReceiptOptionsChange</b>

<b>OnActivityLoggingConfigChange</b>

<b>OnSecurityConfigChange</b>

<b>OnEventLoggingConfigChange</b>

<b>OnOutgoingQueueConfigChange</b>

<b>OnOutgoingArchiveConfigChange</b>

<b>OnIncomingArchiveConfigChange</b>

<b>OnDevicesConfigChange</b>

<b>OnOutboundRoutingGroupsConfigChange</b>

<b>OnOutboundRoutingRulesConfigChange</b>

</td>
</tr>
<tr>
<td>
fsetACTIVITY

</td>
<td>
<b>OnServerActivityChange</b>

</td>
</tr>
<tr>
<td>
fsetQUEUE_STATE

</td>
<td>
<b>OnQueuesStatusChange</b>

</td>
</tr>
<tr>
<td>
fsetIN_ARCHIVE

</td>
<td>
<b>OnIncomingMessageAdded</b>

<b>OnIncomingMessageRemoved</b>

</td>
</tr>
<tr>
<td>
fsetOUT_ARCHIVE

</td>
<td>
<b>OnOutgoingMessageAdded</b>

<b>OnOutgoingMessageRemoved</b>

</td>
</tr>
<tr>
<td>
fsetFXSSVC_ENDED

</td>
<td>
<b>OnServerShutDown</b>

</td>
</tr>
<tr>
<td>
fsetDEVICE_STATUS

</td>
<td>
<b>OnDeviceStatusChange</b>

</td>
</tr>
<tr>
<td>
fsetINCOMING_CALL

</td>
<td>
<b>OnNewCall</b>

</td>
</tr>
</table>
 

The following table lists the <a href="https://msdn.microsoft.com/ebd959d0-516c-46a0-95cc-78aa49d50cc1">IFaxServerNotify2</a> methods called by each member.

<table class="clsStd">
<tr>
<th>Name</th>
<th>
<a href="https://msdn.microsoft.com/ebd959d0-516c-46a0-95cc-78aa49d50cc1">IFaxServerNotify2</a> method called</th>
</tr>
<tr>
<td>
fsetNONE

</td>
<td>
None

</td>
</tr>
<tr>
<td>
fsetIN_QUEUE

</td>
<td>
<b>OnIncomingJobAdded</b>

<b>OnIncomingJobRemoved</b>

<b>OnIncomingJobChanged</b>

</td>
</tr>
<tr>
<td>
fsetOUT_QUEUE

</td>
<td>
<b>OnOutgoingJobAdded</b>

<b>OnOutgoingJobRemoved</b>

<b>OnOutgoingJobChanged</b>

</td>
</tr>
<tr>
<td>
fsetCONFIG

</td>
<td>
<b>OnReceiptOptionsChange</b>

<b>OnActivityLoggingConfigChange</b>

<b>OnSecurityConfigChange</b>

<b>OnEventLoggingConfigChange</b>

<b>OnOutgoingQueueConfigChange</b>

<b>OnOutgoingArchiveConfigChange</b>

<b>OnIncomingArchiveConfigChange</b>

<b>OnDevicesConfigChange</b>

<b>OnOutboundRoutingGroupsConfigChange</b>

<b>OnOutboundRoutingRulesConfigChange</b>

<b>OnGeneralServerConfigChanged</b>

</td>
</tr>
<tr>
<td>
fsetACTIVITY

</td>
<td>
<b>OnServerActivityChange</b>

</td>
</tr>
<tr>
<td>
fsetQUEUE_STATE

</td>
<td>
<b>OnQueuesStatusChange</b>

</td>
</tr>
<tr>
<td>
fsetIN_ARCHIVE

</td>
<td>
<b>OnIncomingMessageAdded</b>

<b>OnIncomingMessageRemoved</b>

</td>
</tr>
<tr>
<td>
fsetOUT_ARCHIVE

</td>
<td>
<b>OnOutgoingMessageAdded</b>

<b>OnOutgoingMessageRemoved</b>

</td>
</tr>
<tr>
<td>
fsetFXSSVC_ENDED

</td>
<td>
<b>OnServerShutDown</b>

</td>
</tr>
<tr>
<td>
fsetDEVICE_STATUS

</td>
<td>
<b>OnDeviceStatusChange</b>

</td>
</tr>
<tr>
<td>
fsetINCOMING_CALL

</td>
<td>
<b>OnNewCall</b>

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9850a677-6ae0-4780-8655-90a8d81fe765">IFaxServer::ListenToServerEvents</a>



<a href="https://msdn.microsoft.com/e8192f70-b0aa-4055-b67b-ff95991b66f2">IFaxServerNotify</a>
 

 

