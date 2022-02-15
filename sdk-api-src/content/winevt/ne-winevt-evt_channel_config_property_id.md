---
UID: NE:winevt._EVT_CHANNEL_CONFIG_PROPERTY_ID
title: EVT_CHANNEL_CONFIG_PROPERTY_ID (winevt.h)
description: Defines the identifiers that identify the configuration properties of a channel.
helpviewer_keywords: ["EVT_CHANNEL_CONFIG_PROPERTY_ID","EVT_CHANNEL_CONFIG_PROPERTY_ID enumeration [EventLog]","EvtChannelConfigAccess","EvtChannelConfigClassicEventlog","EvtChannelConfigEnabled","EvtChannelConfigIsolation","EvtChannelConfigOwningPublisher","EvtChannelConfigPropertyIdEND","EvtChannelConfigType","EvtChannelLoggingConfigAutoBackup","EvtChannelLoggingConfigLogFilePath","EvtChannelLoggingConfigMaxSize","EvtChannelLoggingConfigRetention","EvtChannelPublisherList","EvtChannelPublishingConfigBufferSize","EvtChannelPublishingConfigClockType","EvtChannelPublishingConfigControlGuid","EvtChannelPublishingConfigFileMax","EvtChannelPublishingConfigKeywords","EvtChannelPublishingConfigLatency","EvtChannelPublishingConfigLevel","EvtChannelPublishingConfigMaxBuffers","EvtChannelPublishingConfigMinBuffers","EvtChannelPublishingConfigSidType","wes.evt_channel_config_property_id","winevt/EVT_CHANNEL_CONFIG_PROPERTY_ID","winevt/EvtChannelConfigAccess","winevt/EvtChannelConfigClassicEventlog","winevt/EvtChannelConfigEnabled","winevt/EvtChannelConfigIsolation","winevt/EvtChannelConfigOwningPublisher","winevt/EvtChannelConfigPropertyIdEND","winevt/EvtChannelConfigType","winevt/EvtChannelLoggingConfigAutoBackup","winevt/EvtChannelLoggingConfigLogFilePath","winevt/EvtChannelLoggingConfigMaxSize","winevt/EvtChannelLoggingConfigRetention","winevt/EvtChannelPublisherList","winevt/EvtChannelPublishingConfigBufferSize","winevt/EvtChannelPublishingConfigClockType","winevt/EvtChannelPublishingConfigControlGuid","winevt/EvtChannelPublishingConfigFileMax","winevt/EvtChannelPublishingConfigKeywords","winevt/EvtChannelPublishingConfigLatency","winevt/EvtChannelPublishingConfigLevel","winevt/EvtChannelPublishingConfigMaxBuffers","winevt/EvtChannelPublishingConfigMinBuffers","winevt/EvtChannelPublishingConfigSidType"]
old-location: wes\evt_channel_config_property_id.htm
tech.root: wes
ms.assetid: ea17cbf8-ab60-4bf9-b0a2-998814a50bd0
ms.date: 12/05/2018
ms.keywords: EVT_CHANNEL_CONFIG_PROPERTY_ID, EVT_CHANNEL_CONFIG_PROPERTY_ID enumeration [EventLog], EvtChannelConfigAccess, EvtChannelConfigClassicEventlog, EvtChannelConfigEnabled, EvtChannelConfigIsolation, EvtChannelConfigOwningPublisher, EvtChannelConfigPropertyIdEND, EvtChannelConfigType, EvtChannelLoggingConfigAutoBackup, EvtChannelLoggingConfigLogFilePath, EvtChannelLoggingConfigMaxSize, EvtChannelLoggingConfigRetention, EvtChannelPublisherList, EvtChannelPublishingConfigBufferSize, EvtChannelPublishingConfigClockType, EvtChannelPublishingConfigControlGuid, EvtChannelPublishingConfigFileMax, EvtChannelPublishingConfigKeywords, EvtChannelPublishingConfigLatency, EvtChannelPublishingConfigLevel, EvtChannelPublishingConfigMaxBuffers, EvtChannelPublishingConfigMinBuffers, EvtChannelPublishingConfigSidType, wes.evt_channel_config_property_id, winevt/EVT_CHANNEL_CONFIG_PROPERTY_ID, winevt/EvtChannelConfigAccess, winevt/EvtChannelConfigClassicEventlog, winevt/EvtChannelConfigEnabled, winevt/EvtChannelConfigIsolation, winevt/EvtChannelConfigOwningPublisher, winevt/EvtChannelConfigPropertyIdEND, winevt/EvtChannelConfigType, winevt/EvtChannelLoggingConfigAutoBackup, winevt/EvtChannelLoggingConfigLogFilePath, winevt/EvtChannelLoggingConfigMaxSize, winevt/EvtChannelLoggingConfigRetention, winevt/EvtChannelPublisherList, winevt/EvtChannelPublishingConfigBufferSize, winevt/EvtChannelPublishingConfigClockType, winevt/EvtChannelPublishingConfigControlGuid, winevt/EvtChannelPublishingConfigFileMax, winevt/EvtChannelPublishingConfigKeywords, winevt/EvtChannelPublishingConfigLatency, winevt/EvtChannelPublishingConfigLevel, winevt/EvtChannelPublishingConfigMaxBuffers, winevt/EvtChannelPublishingConfigMinBuffers, winevt/EvtChannelPublishingConfigSidType
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EVT_CHANNEL_CONFIG_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_CHANNEL_CONFIG_PROPERTY_ID
 - winevt/_EVT_CHANNEL_CONFIG_PROPERTY_ID
 - EVT_CHANNEL_CONFIG_PROPERTY_ID
 - winevt/EVT_CHANNEL_CONFIG_PROPERTY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_CHANNEL_CONFIG_PROPERTY_ID
---

# EVT_CHANNEL_CONFIG_PROPERTY_ID enumeration


## -description

Defines the identifiers that identify the configuration properties of a channel.

## -enum-fields

### -field EvtChannelConfigEnabled:0

Identifies the <b>enabled</b> attribute of the channel.  The variant type for this property is <b>EvtVarTypeBoolean</b>.

You cannot set this property for the Application, System, and Security channels.

### -field EvtChannelConfigIsolation

Identifies the <b>isolation</b> attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. For possible isolation values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_channel_isolation_type">EVT_CHANNEL_ISOLATION_TYPE</a> enumeration.

You cannot set this property for the Application, System, and Security channels.

### -field EvtChannelConfigType

Identifies the <b>type</b> attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. For possible isolation values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_channel_type">EVT_CHANNEL_TYPE</a> enumeration. 

You cannot set this property.

### -field EvtChannelConfigOwningPublisher

Identifies the <b>name</b> attribute of the provider that defined the channel.  The variant type for this property is <b>EvtVarTypeString</b>. 

You cannot set this property.

### -field EvtChannelConfigClassicEventlog

Identifies the configuration property that indicates whether the channel is a classic event channel (for example the Application or System log). The variant type for this property is <b>EvtVarTypeBoolean</b>. 

You cannot set this property.

### -field EvtChannelConfigAccess

Identifies the <b>access</b> attribute of the channel.  The variant type for this property is <b>EvtVarTypeString</b>.

### -field EvtChannelLoggingConfigRetention

Identifies the <b>retention</b> logging attribute of the channel.  The variant type for this property is <b>EvtVarTypeBoolean</b>.

### -field EvtChannelLoggingConfigAutoBackup

Identifies the <b>autoBackup</b> logging attribute of the channel.  The variant type for this property is <b>EvtVarTypeBoolean</b>.

### -field EvtChannelLoggingConfigMaxSize

Identifies the <b>maxSize</b> logging attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt64</b>.

### -field EvtChannelLoggingConfigLogFilePath

Identifies the configuration property that contains the path to the file that backs the channel. The variant type for this property is <b>EvtVarTypeString</b>.

### -field EvtChannelPublishingConfigLevel

Identifies the <b>level</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. 

To set this property, you must first disable the debug or analytic channel.

### -field EvtChannelPublishingConfigKeywords

Identifies the <b>keywords</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt64</b>. 

To set this property, you must first disable the debug or analytic channel.

### -field EvtChannelPublishingConfigControlGuid

Identifies the <b>controlGuid</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeGuid</b>. 

You cannot set this property.

### -field EvtChannelPublishingConfigBufferSize

Identifies the <b>bufferSize</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. 

You cannot set this property.

### -field EvtChannelPublishingConfigMinBuffers

Identifies the <b>minBuffers</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. 

You cannot set this property.

### -field EvtChannelPublishingConfigMaxBuffers

Identifies the <b>maxBuffers</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. 

You cannot set this property.

### -field EvtChannelPublishingConfigLatency

Identifies the <b>latency</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. 

You cannot set this property.

### -field EvtChannelPublishingConfigClockType

Identifies the <b>clockType</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. For possible clock type values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_channel_clock_type">EVT_CHANNEL_CLOCK_TYPE</a> enumeration. 

You cannot set this property.

### -field EvtChannelPublishingConfigSidType

Identifies the <b>sidType</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. For possible SID type values, see the  <a href="/windows/desktop/api/winevt/ne-winevt-evt_channel_sid_type">EVT_CHANNEL_SID_TYPE</a> enumeration. 

You cannot set this property.

### -field EvtChannelPublisherList

Identifies the configuration property that contains the list of providers that import this channel.  The variant type for this property is <b>EvtVarTypeString | EVT_VARIANT_TYPE_ARRAY</b>. 

You cannot set this property.

### -field EvtChannelPublishingConfigFileMax

Identifies the <b>fileMax</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>.

### -field EvtChannelConfigPropertyIdEND

This enumeration value marks the end of the enumeration values.

## -see-also

<a href="/windows/desktop/WES/eventmanifestschema-channelloggingtype-complextype">ChannelLoggingType Complex Type</a>



<a href="/windows/desktop/WES/eventmanifestschema-channelpublishingtype-complextype">ChannelPublishingType Complex Type</a>



<a href="/windows/desktop/WES/eventmanifestschema-channeltype-complextype">ChannelType Complex Type</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtgetchannelconfigproperty">EvtGetChannelConfigProperty</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty">EvtSetChannelConfigProperty</a>
