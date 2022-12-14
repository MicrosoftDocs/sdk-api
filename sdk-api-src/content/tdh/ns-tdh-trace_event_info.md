---
UID: NS:tdh._TRACE_EVENT_INFO
title: TRACE_EVENT_INFO (tdh.h)
description: Defines the information about the event.
helpviewer_keywords: ["*PTRACE_EVENT_INFO","TRACE_EVENT_INFO","TRACE_EVENT_INFO structure [ETW]","etw.trace_event_info_struct","tdh.trace_event_info_struct","tdh/TRACE_EVENT_INFO"]
old-location: etw\trace_event_info_struct.htm
tech.root: ETW
ms.assetid: ecf57a23-0dd2-4954-82ac-e92f651c226f
ms.date: 12/05/2018
ms.keywords: '*PTRACE_EVENT_INFO, TRACE_EVENT_INFO, TRACE_EVENT_INFO structure [ETW], etw.trace_event_info_struct, tdh.trace_event_info_struct, tdh/TRACE_EVENT_INFO'
req.header: tdh.h
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
req.typenames: TRACE_EVENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRACE_EVENT_INFO
 - tdh/_TRACE_EVENT_INFO
 - TRACE_EVENT_INFO
 - tdh/TRACE_EVENT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - TRACE_EVENT_INFO
---

# TRACE_EVENT_INFO structure


## -description

Defines the information about the event.

## -struct-fields

### -field ProviderGuid

A GUID that identifies the provider.

### -field EventGuid

A GUID that identifies the MOF class that contains the event. If the provider uses a manifest to define its events, this member is GUID_NULL.

### -field EventDescriptor

A <a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a> structure that describes the event.

### -field DecodingSource

A <a href="/windows/desktop/api/tdh/ne-tdh-decoding_source">DECODING_SOURCE</a> enumeration value that identifies the source used to parse the event's data (for example, an instrumentation manifest of WMI MOF class).

### -field ProviderNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the provider.

### -field LevelNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the level. For possible names, see Remarks in <a href="/windows/desktop/WES/eventmanifestschema-leveltype-complextype">LevelType</a>.

### -field ChannelNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the channel. For possible names, see Remarks in <a href="/windows/desktop/WES/eventmanifestschema-channeltype-complextype">ChannelType</a>.

### -field KeywordsNameOffset

The offset from the beginning of this structure to a list of null-terminated Unicode strings that contains the names of the keywords. The list is terminated with two NULL characters. For possible names, see Remarks in <a href="/windows/desktop/WES/eventmanifestschema-keywordtype-complextype">KeywordType</a>.

### -field TaskNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the task. For possible names, see Remarks in <a href="/windows/desktop/WES/eventmanifestschema-tasktype-complextype">TaskType</a>.

### -field OpcodeNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the operation. For possible names, see Remarks in <a href="/windows/desktop/WES/eventmanifestschema-opcodetype-complextype">OpcodeType</a>.

### -field EventMessageOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the event message string.  The offset is zero if there is no message string. For information on message strings, see the <b>message</b> attribute for <a href="/windows/desktop/WES/eventmanifestschema-eventdefinitiontype-complextype">EventDefinitionType</a>.

The message string can contain insert sequences, for example, Unable to connect to the %1 printer. The number of the insert sequence identifies the property in the event data to use for the substitution.

### -field ProviderMessageOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the localized provider name.

### -field BinaryXMLOffset

Reserved.

### -field BinaryXMLSize

Reserved.

### -field EventNameOffset

### -field ActivityIDNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the property name of the activity identifier in the MOF class. Supported for classic ETW events only.

### -field EventAttributesOffset

### -field RelatedActivityIDNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the property name of the related activity identifier in the MOF class. Supported for legacy ETW events only.

### -field PropertyCount

The number of elements in the <b>EventPropertyInfoArray</b> array.

### -field TopLevelPropertyCount

The number of properties in the <b>EventPropertyInfoArray</b> array that are top-level properties. This number does not include members of structures. Top-level properties come before all member properties in the array.

### -field Flags

Reserved.

### -field Reserved

### -field Tags

A 28-bit value associated with the event metadata. This value can be used by the event provider to associate additional semantic data with an event for use by an event processing tool. For example, a tag value of 5 might indicate that the event contains debugging information. The semantics of any values in this field are defined by the event provider.

### -field EventPropertyInfoArray

An array of <a href="/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a> structures that provides information about each property of the event's user data.

## -remarks

The value of an offset is zero if the member is not defined.

## -see-also
<a href="/windows/desktop/WES/eventmanifestschema-channeltype-complextype">ChannelType</a>



<a href="/windows/desktop/api/tdh/ne-tdh-decoding_source">DECODING_SOURCE</a>



<a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>



<a href="/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a>



<a href="/windows/desktop/WES/eventmanifestschema-eventdefinitiontype-complextype">EventDefinitionType</a>



<a href="/windows/desktop/WES/eventmanifestschema-keywordtype-complextype">KeywordType</a>



<a href="/windows/desktop/WES/eventmanifestschema-leveltype-complextype">LevelType</a>



<a href="/windows/desktop/WES/eventmanifestschema-opcodetype-complextype">OpcodeType</a>



<a href="/windows/desktop/WES/eventmanifestschema-tasktype-complextype">TaskType</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhenumeratemanifestproviderevents">TdhEnumerateManifestProviderEvents</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhgeteventinformation">TdhGetEventInformation</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhgetmanifesteventinformation">TdhGetManifestEventInformation</a>