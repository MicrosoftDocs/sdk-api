---
UID: NS:tdh._EVENT_PROPERTY_INFO
title: EVENT_PROPERTY_INFO (tdh.h)
description: Provides information about a single property of the event or filter.
helpviewer_keywords: ["*PEVENT_PROPERTY_INFO","EVENT_PROPERTY_INFO","EVENT_PROPERTY_INFO structure [ETW]","etw.event_property_info_struct","tdh.event_property_info_struct","tdh/EVENT_PROPERTY_INFO"]
old-location: etw\event_property_info_struct.htm
tech.root: ETW
ms.assetid: 06b82b31-1f0e-45d5-88ec-9b9835af10df
ms.date: 12/05/2018
ms.keywords: '*PEVENT_PROPERTY_INFO, EVENT_PROPERTY_INFO, EVENT_PROPERTY_INFO structure [ETW], etw.event_property_info_struct, tdh.event_property_info_struct, tdh/EVENT_PROPERTY_INFO'
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
req.typenames: EVENT_PROPERTY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_PROPERTY_INFO
 - tdh/_EVENT_PROPERTY_INFO
 - EVENT_PROPERTY_INFO
 - tdh/EVENT_PROPERTY_INFO
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
 - EVENT_PROPERTY_INFO
---

# EVENT_PROPERTY_INFO structure


## -description

Provides information about a single property of the event or filter.

## -struct-fields

### -field Flags

Flags that indicate if the property is contained in a structure or array. For possible values, see the <a href="/windows/desktop/api/tdh/ne-tdh-property_flags">PROPERTY_FLAGS</a> enumeration.

### -field NameOffset

Offset to a null-terminated Unicode string that contains the name of the property. If this an event property, the offset is from the beginning of the <a href="/windows/desktop/api/tdh/ns-tdh-trace_event_info">TRACE_EVENT_INFO</a> structure. If this is a filter property, the offset is from the beginning of the <a href="/windows/desktop/api/tdh/ns-tdh-provider_filter_info">PROVIDER_FILTER_INFO</a> structure.

### -field nonStructType

Use these members if the <a href="/windows/desktop/api/tdh/ne-tdh-property_flags">PropertyStruct</a> flag in <b>Flags</b> is not set; otherwise, use the <b>structType</b> member.

### -field nonStructType.InType

Data type of this property on input. For a description of these types, see Remarks in  <a href="/windows/desktop/WES/eventmanifestschema-inputtype-complextype">InputType</a>.

For descriptions of these types, see <a href="/windows/desktop/ETW/event-tracing-mof-qualifiers">Event Tracing MOF Qualifiers</a>.

<a href="/windows/desktop/api/tdh/nf-tdh-tdhgetpropertysize">TdhGetPropertySize</a>
<a href="/windows/desktop/api/tdh/nf-tdh-tdhgetpropertysize">TdhGetPropertySize</a>

### -field nonStructType.OutType

Output format for this property. If the value is TDH_OUTTYPE_NULL, use the in type  as the output format. For a description of these types, see Remarks in <a href="/windows/desktop/WES/eventmanifestschema-inputtype-complextype">InputType</a>.

For descriptions of these types, see <a href="/windows/desktop/ETW/event-tracing-mof-qualifiers">Event Tracing MOF Qualifiers</a>.

### -field nonStructType.MapNameOffset

Offset from the beginning of the <a href="/windows/desktop/api/tdh/ns-tdh-trace_event_info">TRACE_EVENT_INFO</a> structure to a null-terminated Unicode string that contains the name of the map attribute value. You can pass this string to <a href="/windows/desktop/api/tdh/nf-tdh-tdhgeteventmapinformation">TdhGetEventMapInformation</a> to retrieve information about the value map.

### -field structType

Use these members if the <a href="/windows/desktop/api/tdh/ne-tdh-property_flags">PropertyStruct</a> flag in <b>Flags</b> is set; otherwise, use the <b>nonStructType</b> member.

### -field structType.StructStartIndex

Zero-based index to the element of the property array that contains the first member of the structure.

### -field structType.NumOfStructMembers

Number of members in the structure.

### -field structType.padding

Not used.

### -field customSchemaType

Use these members if the <b>PropertyHasCustomSchema</b> flag in <b>Flags</b> is set; otherwise, use the <b>nonStructType</b> member.

### -field customSchemaType.padding2

This value is not used for <b>customSchemaType</b>. For compatibility with decoders that do not recognize custom schema properties, this value will contain a TDH InType such as TDH_INTYPE_BINARY.

### -field customSchemaType.OutType

Output format for this property. If the value is TDH_OUTTYPE_NULL, use the in type  as the output format. For a description of these types, see Remarks in <a href="/windows/desktop/WES/eventmanifestschema-inputtype-complextype">InputType</a>.

For descriptions of these types, see <a href="/windows/desktop/ETW/event-tracing-mof-qualifiers">Event Tracing MOF Qualifiers</a>.

### -field customSchemaType.CustomSchemaOffset

Offset (in bytes) from the beginning of the TRACE_EVENT_INFO structure to the custom schema information. The custom schema information will contain a 2-byte protocol identifier, followed by a 2-byte schema length, followed by the schema.

### -field count

Number of elements in the array. Note that this value is 1 for properties that are not defined as an array.

### -field countPropertyIndex

Zero-based index to the element of the property array that contains the number of elements in the array. Use this member if the <a href="/windows/desktop/api/tdh/ne-tdh-property_flags">PropertyParamCount</a> flag in <b>Flags</b> is set; otherwise, use the <b>count</b> member.

### -field length

Size of the property, in bytes. Note that variable-sized types such as strings and binary data have a length of zero unless the property has length attribute to explicitly indicate its real length. Structures have a length of zero.

### -field lengthPropertyIndex

Zero-based index to the element of the property array that contains the size value of this property. Use this member if the <a href="/windows/desktop/api/tdh/ne-tdh-property_flags">PropertyParamLength</a> flag in <b>Flags</b> is set; otherwise, use the <b>length</b> member.

### -field Reserved

Reserved.

### -field Tags

A 28-bit value associated with the field metadata. This value is valid only if the <i>PropertyHasTags</i> flag is set. This value can be used by the event provider to associate additional semantic data with a field for use by an event processing tool. For example, a tag value of 1 might indicate that the field contains a username. The semantics of any values in this field are defined by the event provider.

## -remarks

Filters do not support maps, structures, or arrays.

## -see-also
<a href="/windows/desktop/api/tdh/ns-tdh-provider_filter_info">PROVIDER_FILTER_INFO</a>



<a href="/windows/desktop/api/tdh/ns-tdh-trace_event_info">TRACE_EVENT_INFO</a>