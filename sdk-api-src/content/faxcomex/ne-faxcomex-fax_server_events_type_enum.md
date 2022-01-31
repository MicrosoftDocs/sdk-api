---
UID: NE:faxcomex.FAX_SERVER_EVENTS_TYPE_ENUM
title: FAX_SERVER_EVENTS_TYPE_ENUM (faxcomex.h)
description: The FAX_SERVER_EVENTS_TYPE_ENUM enumeration defines the types of events the fax service sends to client applications that are listening for events. The members of this enumeration are bit values and can be used in combination.
helpviewer_keywords: ["FAX_SERVER_EVENTS_TYPE_ENUM","FAX_SERVER_EVENTS_TYPE_ENUM enumeration [Fax Service]","_mfax_fax_server_events_type_enum","fax._mfax_fax_server_events_type_enum","faxcomex/FAX_SERVER_EVENTS_TYPE_ENUM","faxcomex/fsetACTIVITY","faxcomex/fsetCONFIG","faxcomex/fsetDEVICE_STATUS","faxcomex/fsetFXSSVC_ENDED","faxcomex/fsetINCOMING_CALL","faxcomex/fsetIN_ARCHIVE","faxcomex/fsetIN_QUEUE","faxcomex/fsetNONE","faxcomex/fsetOUT_ARCHIVE","faxcomex/fsetOUT_QUEUE","faxcomex/fsetQUEUE_STATE","fsetACTIVITY","fsetCONFIG","fsetDEVICE_STATUS","fsetFXSSVC_ENDED","fsetINCOMING_CALL","fsetIN_ARCHIVE","fsetIN_QUEUE","fsetNONE","fsetOUT_ARCHIVE","fsetOUT_QUEUE","fsetQUEUE_STATE"]
old-location: fax\_mfax_fax_server_events_type_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_61t9.htm
ms.date: 12/05/2018
ms.keywords: FAX_SERVER_EVENTS_TYPE_ENUM, FAX_SERVER_EVENTS_TYPE_ENUM enumeration [Fax Service], _mfax_fax_server_events_type_enum, fax._mfax_fax_server_events_type_enum, faxcomex/FAX_SERVER_EVENTS_TYPE_ENUM, faxcomex/fsetACTIVITY, faxcomex/fsetCONFIG, faxcomex/fsetDEVICE_STATUS, faxcomex/fsetFXSSVC_ENDED, faxcomex/fsetINCOMING_CALL, faxcomex/fsetIN_ARCHIVE, faxcomex/fsetIN_QUEUE, faxcomex/fsetNONE, faxcomex/fsetOUT_ARCHIVE, faxcomex/fsetOUT_QUEUE, faxcomex/fsetQUEUE_STATE, fsetACTIVITY, fsetCONFIG, fsetDEVICE_STATUS, fsetFXSSVC_ENDED, fsetINCOMING_CALL, fsetIN_ARCHIVE, fsetIN_QUEUE, fsetNONE, fsetOUT_ARCHIVE, fsetOUT_QUEUE, fsetQUEUE_STATE
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: FAX_SERVER_EVENTS_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_SERVER_EVENTS_TYPE_ENUM
 - faxcomex/FAX_SERVER_EVENTS_TYPE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_SERVER_EVENTS_TYPE_ENUM
---

# FAX_SERVER_EVENTS_TYPE_ENUM enumeration


## -description

The <b>FAX_SERVER_EVENTS_TYPE_ENUM</b> enumeration defines the types of events the fax service sends to client applications that are listening for events. The members of this enumeration are bit values and can be used in combination.

## -enum-fields

### -field fsetNONE:0

No events are sent.

### -field fsetIN_QUEUE:0x1

The client requests notifications about fax jobs in the incoming queue. When the status of an incoming fax job changes, the fax service issues a notification of this type.

### -field fsetOUT_QUEUE:0x2

The client requests notification about fax jobs in the outgoing queue. When the status of an outgoing fax job changes, the fax service issues a notification of this type.

### -field fsetCONFIG:0x4

The client requests notifications about changes to the fax server configuration. When the configuration data changes, the fax service issues a notification of this type.

### -field fsetACTIVITY:0x8

The client requests notifications about the fax server activity. When the activity status of the fax server changes, the fax service issues a notification of this type.

### -field fsetQUEUE_STATE:0x10

The client requests notifications about changes in the status of the fax job queue. When the status of the queue changes, the fax service issues a notification.

### -field fsetIN_ARCHIVE:0x20

The client requests notifications about the addition or removal of fax messages from the incoming archive. When a message is removed from the archive, the fax service issues a notification. The notification includes the archive type (inbound) and the unique ID of the fax message.

### -field fsetOUT_ARCHIVE:0x40

The client requests notifications about the addition or removal of fax messages from the outgoing archive. When a message is removed from the archive, the fax service issues a notification. The notification includes the archive type (outbound) and the unique ID of the fax message.

### -field fsetFXSSVC_ENDED:0x80

The client requests notifications when the fax service stops executing.

### -field fsetDEVICE_STATUS:0x100

The client requests notifications when a device status changes.

### -field fsetINCOMING_CALL:0x200

The client requests notifications when there is an incoming call.

## -remarks

The following table lists the <a href="/windows/desktop/api/faxcomex/nn-faxcomex-ifaxservernotify2">IFaxServerNotify</a> methods called by each member.

<table class="clsStd">
<tr>
<th>Name</th>
<th>
<a href="/windows/desktop/api/faxcomex/nn-faxcomex-ifaxservernotify2">IFaxServerNotify</a> method called</th>
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
 

The following table lists the <a href="/windows/win32/api/faxcomex/nn-faxcomex-_ifaxservernotify2">IFaxServerNotify2</a> methods called by each member.

<table class="clsStd">
<tr>
<th>Name</th>
<th>
<a href="/windows/win32/api/faxcomex/nn-faxcomex-_ifaxservernotify2">IFaxServerNotify2</a> method called</th>
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

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-listentoserverevents-vb">IFaxServer::ListenToServerEvents</a>



<a href="/windows/desktop/api/faxcomex/nn-faxcomex-ifaxservernotify2">IFaxServerNotify</a>
