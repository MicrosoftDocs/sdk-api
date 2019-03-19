---
UID: NE:winevt._EVT_CHANNEL_CONFIG_PROPERTY_ID
title: EVT_CHANNEL_CONFIG_PROPERTY_ID (winevt.h)
author: windows-sdk-content
description: Defines the identifiers that identify the configuration properties of a channel.
old-location: wes\evt_channel_config_property_id.htm
tech.root: wes
ms.assetid: ea17cbf8-ab60-4bf9-b0a2-998814a50bd0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EVT_CHANNEL_CONFIG_PROPERTY_ID, EVT_CHANNEL_CONFIG_PROPERTY_ID enumeration [EventLog], EvtChannelConfigAccess, EvtChannelConfigClassicEventlog, EvtChannelConfigEnabled, EvtChannelConfigIsolation, EvtChannelConfigOwningPublisher, EvtChannelConfigPropertyIdEND, EvtChannelConfigType, EvtChannelLoggingConfigAutoBackup, EvtChannelLoggingConfigLogFilePath, EvtChannelLoggingConfigMaxSize, EvtChannelLoggingConfigRetention, EvtChannelPublisherList, EvtChannelPublishingConfigBufferSize, EvtChannelPublishingConfigClockType, EvtChannelPublishingConfigControlGuid, EvtChannelPublishingConfigFileMax, EvtChannelPublishingConfigKeywords, EvtChannelPublishingConfigLatency, EvtChannelPublishingConfigLevel, EvtChannelPublishingConfigMaxBuffers, EvtChannelPublishingConfigMinBuffers, EvtChannelPublishingConfigSidType, wes.evt_channel_config_property_id, winevt/EVT_CHANNEL_CONFIG_PROPERTY_ID, winevt/EvtChannelConfigAccess, winevt/EvtChannelConfigClassicEventlog, winevt/EvtChannelConfigEnabled, winevt/EvtChannelConfigIsolation, winevt/EvtChannelConfigOwningPublisher, winevt/EvtChannelConfigPropertyIdEND, winevt/EvtChannelConfigType, winevt/EvtChannelLoggingConfigAutoBackup, winevt/EvtChannelLoggingConfigLogFilePath, winevt/EvtChannelLoggingConfigMaxSize, winevt/EvtChannelLoggingConfigRetention, winevt/EvtChannelPublisherList, winevt/EvtChannelPublishingConfigBufferSize, winevt/EvtChannelPublishingConfigClockType, winevt/EvtChannelPublishingConfigControlGuid, winevt/EvtChannelPublishingConfigFileMax, winevt/EvtChannelPublishingConfigKeywords, winevt/EvtChannelPublishingConfigLatency, winevt/EvtChannelPublishingConfigLevel, winevt/EvtChannelPublishingConfigMaxBuffers, winevt/EvtChannelPublishingConfigMinBuffers, winevt/EvtChannelPublishingConfigSidType
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_CHANNEL_CONFIG_PROPERTY_ID
product: Windows
targetos: Windows
req.typenames: EVT_CHANNEL_CONFIG_PROPERTY_ID
req.redist: 
---

# EVT_CHANNEL_CONFIG_PROPERTY_ID enumeration


## -description


Defines the identifiers that identify the configuration properties of a channel.


## -enum-fields




### -field EvtChannelConfigEnabled

Identifies the <b>enabled</b> attribute of the channel.  The variant type for this property is <b>EvtVarTypeBoolean</b>.

You cannot set this property for the Application, System, and Security channels.


### -field EvtChannelConfigIsolation

Identifies the <b>isolation</b> attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. For possible isolation values, see the <a href="https://msdn.microsoft.com/63b01c20-f413-451d-b34d-b2496ebf8181">EVT_CHANNEL_ISOLATION_TYPE</a> enumeration.

You cannot set this property for the Application, System, and Security channels.


### -field EvtChannelConfigType

Identifies the <b>type</b> attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. For possible isolation values, see the <a href="https://msdn.microsoft.com/5650dd28-b0ef-4d74-abc6-85ed2bd56b38">EVT_CHANNEL_TYPE</a> enumeration. 

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

Identifies the <b>clockType</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. For possible clock type values, see the <a href="https://msdn.microsoft.com/575a6667-b832-46e8-8704-0612e04b8669">EVT_CHANNEL_CLOCK_TYPE</a> enumeration. 

You cannot set this property.


### -field EvtChannelPublishingConfigSidType

Identifies the <b>sidType</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>. For possible SID type values, see the  <a href="https://msdn.microsoft.com/7eadae8f-71b4-44de-ba66-0e460fee496c">EVT_CHANNEL_SID_TYPE</a> enumeration. 

You cannot set this property.


### -field EvtChannelPublisherList

Identifies the configuration property that contains the list of providers that import this channel.  The variant type for this property is <b>EvtVarTypeString | EVT_VARIANT_TYPE_ARRAY</b>. 

You cannot set this property.


### -field EvtChannelPublishingConfigFileMax

Identifies the <b>fileMax</b> publishing attribute of the channel.  The variant type for this property is <b>EvtVarTypeUInt32</b>.


### -field EvtChannelConfigPropertyIdEND

This enumeration value marks the end of the enumeration values.


## -see-also




<a href="https://msdn.microsoft.com/58da75dd-d303-4a57-8c9b-5fde575c3cbb">ChannelLoggingType Complex Type</a>



<a href="https://msdn.microsoft.com/4b3980f4-8652-4070-97c0-99cd1a9fc85a">ChannelPublishingType Complex Type</a>



<a href="https://msdn.microsoft.com/882506e5-222b-45c8-af4b-59db8baa1dae">ChannelType Complex Type</a>



<a href="https://msdn.microsoft.com/0f84f51c-716e-4a70-b31c-2b4f40b3fd83">EvtGetChannelConfigProperty</a>



<a href="https://msdn.microsoft.com/f5f11bd9-5eb0-4afe-8c8b-57fa3850ad56">EvtSetChannelConfigProperty</a>
 

 

