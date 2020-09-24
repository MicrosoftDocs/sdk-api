---
UID: NE:winevt._EVT_EVENT_METADATA_PROPERTY_ID
title: EVT_EVENT_METADATA_PROPERTY_ID (winevt.h)
description: Defines the identifiers that identify the metadata properties of an event definition.
helpviewer_keywords: ["EVT_EVENT_METADATA_PROPERTY_ID","EVT_EVENT_METADATA_PROPERTY_ID enumeration [EventLog]","EventMetadataEventChannel","EventMetadataEventID","EventMetadataEventKeyword","EventMetadataEventLevel","EventMetadataEventMessageID","EventMetadataEventOpcode","EventMetadataEventTask","EventMetadataEventTemplate","EventMetadataEventVersion","EvtEventMetadataPropertyIdEND","wes.evt_event_metadata_property_id","winevt/EVT_EVENT_METADATA_PROPERTY_ID","winevt/EventMetadataEventChannel","winevt/EventMetadataEventID","winevt/EventMetadataEventKeyword","winevt/EventMetadataEventLevel","winevt/EventMetadataEventMessageID","winevt/EventMetadataEventOpcode","winevt/EventMetadataEventTask","winevt/EventMetadataEventTemplate","winevt/EventMetadataEventVersion","winevt/EvtEventMetadataPropertyIdEND"]
old-location: wes\evt_event_metadata_property_id.htm
tech.root: wes
ms.assetid: d5a71e51-c080-4976-9f33-fe24b523ae81
ms.date: 12/05/2018
ms.keywords: EVT_EVENT_METADATA_PROPERTY_ID, EVT_EVENT_METADATA_PROPERTY_ID enumeration [EventLog], EventMetadataEventChannel, EventMetadataEventID, EventMetadataEventKeyword, EventMetadataEventLevel, EventMetadataEventMessageID, EventMetadataEventOpcode, EventMetadataEventTask, EventMetadataEventTemplate, EventMetadataEventVersion, EvtEventMetadataPropertyIdEND, wes.evt_event_metadata_property_id, winevt/EVT_EVENT_METADATA_PROPERTY_ID, winevt/EventMetadataEventChannel, winevt/EventMetadataEventID, winevt/EventMetadataEventKeyword, winevt/EventMetadataEventLevel, winevt/EventMetadataEventMessageID, winevt/EventMetadataEventOpcode, winevt/EventMetadataEventTask, winevt/EventMetadataEventTemplate, winevt/EventMetadataEventVersion, winevt/EvtEventMetadataPropertyIdEND
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
req.typenames: EVT_EVENT_METADATA_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_EVENT_METADATA_PROPERTY_ID
 - winevt/_EVT_EVENT_METADATA_PROPERTY_ID
 - EVT_EVENT_METADATA_PROPERTY_ID
 - winevt/EVT_EVENT_METADATA_PROPERTY_ID
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
 - EVT_EVENT_METADATA_PROPERTY_ID
---

# EVT_EVENT_METADATA_PROPERTY_ID enumeration


## -description

Defines the identifiers that identify the metadata properties of an event definition.

## -enum-fields

### -field EventMetadataEventID

Identifies the <b>value</b> attribute of the event definition. The variant type for this property is <b>EvtVarTypeUInt32</b>.

### -field EventMetadataEventVersion

Identifies the <b>version</b> attribute of the event definition. The variant type for this property is <b>EvtVarTypeUInt32</b>.

### -field EventMetadataEventChannel

Identifies the <b>channel</b> attribute of the event definition. The variant type for this property is <b>EvtVarTypeUInt32</b>. This property does not contain the channel identifier that you specified in the event definition but instead contains the <b>value</b> attribute of the channel. The value is zero if the event definition does not specify a channel.

### -field EventMetadataEventLevel

Identifies the <b>level</b> attribute of the event definition. The variant type for this property is <b>EvtVarTypeUInt32</b>. This property does not contain the level name that you specified in the event definition but instead contains the <b>value</b> attribute of the level. The value is zero if the event definition does not specify a level.

### -field EventMetadataEventOpcode

Identifies the <b>opcode</b> attribute of the event definition. The variant type for this property is <b>EvtVarTypeUInt32</b>. This property does not contain the opcode name that you specified in the event definition but instead contains the <b>value</b> attribute of the opcode. The value is zero if the event definition does not specify an opcode.

### -field EventMetadataEventTask

Identifies the <b>task</b> attribute of the event definition. The variant type for this property is <b>EvtVarTypeUInt32</b>. This property does not contain the task name that you specified in the event definition but instead contains the <b>value</b> attribute of the task. The value is zero if the event definition does not specify a task.

### -field EventMetadataEventKeyword

Identifies the <b>keyword</b> attribute of the event definition. The variant type for this property is <b>EvtVarTypeUInt64</b>. This property does not contain the list of keyword names that you specified in the event definition but instead contains a 64-bitmask of all the keywords. The top 16 bits of the mask are reserved for internal use and should be ignored when determining the keyword bits that the event definition set.

### -field EventMetadataEventMessageID

Identifies the <b>message</b> attribute of the event definition. The variant type for this property is <b>EvtVarTypeUInt32</b>. The property contains the resource identifier that is assigned to the message string. To get the message string, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtformatmessage">EvtFormatMessage</a> function. If the event definition does not specify a message, the value is –1.

### -field EventMetadataEventTemplate

Identifies the <b>template</b> attribute of the event definition. The variant type for this property is <b>EvtVarTypeString</b>. This property does not contain the template name that you specified in the event definition but instead contains an XML string that includes the template node and each data node; the string does not include the UserData. The value is an empty string if the event definition does not specify a template.

### -field EvtEventMetadataPropertyIdEND

This enumeration value marks the end of the enumeration values.

## -remarks

The channel, level, opcode, task, and keyword properties return the value of the value attribute. To get the metadata for a property whose value is not zero, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtgetpublishermetadataproperty">EvtGetPublisherMetadataProperty</a> function for the property. For example, to get the metadata for the task property, call <b>EvtGetPublisherMetadataProperty</b> using the EvtPublisherMetadataTasks provider property identifier. The function returns an array of task objects that you enumerate. For each object, compare the value of the object's value property to the value specified in the event. If the values match, use the metadata from that object.

## -see-also

<a href="/windows/desktop/WES/eventmanifestschema-eventdefinitiontype-complextype">EventDefinitionType Complex Type</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtgeteventmetadataproperty">EvtGetEventMetadataProperty</a>