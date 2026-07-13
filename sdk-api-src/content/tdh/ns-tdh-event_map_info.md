---
UID: NS:tdh._EVENT_MAP_INFO
title: EVENT_MAP_INFO (tdh.h)
description: Defines the metadata about the event map.
helpviewer_keywords: ["*PEVENT_MAP_INFO","EVENT_MAP_INFO","EVENT_MAP_INFO structure [ETW]","etw.event_map_info_struct","tdh.event_map_info_struct","tdh/EVENT_MAP_INFO"]
old-location: etw\event_map_info_struct.htm
tech.root: ETW
ms.assetid: dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98
ms.date: 12/05/2018
ms.keywords: '*PEVENT_MAP_INFO, EVENT_MAP_INFO, EVENT_MAP_INFO structure [ETW], etw.event_map_info_struct, tdh.event_map_info_struct, tdh/EVENT_MAP_INFO'
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
req.typenames: EVENT_MAP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_MAP_INFO
 - tdh/_EVENT_MAP_INFO
 - EVENT_MAP_INFO
 - tdh/EVENT_MAP_INFO
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
 - EVENT_MAP_INFO
---

# EVENT_MAP_INFO structure


## -description

Defines the metadata about the event map.

## -struct-fields

### -field NameOffset

Offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the event map.

### -field Flag

Indicates if the map is a value map, bitmap, or pattern map. This member can contain one or more flag values. For possible values, see the <a href="/windows/desktop/api/tdh/ne-tdh-map_flags">MAP_FLAGS</a> enumeration.

### -field EntryCount

Number of map entries in <b>MapEntryArray</b>.

### -field MapEntryValueType

 
		Determines if you use the <b>Value</b> member or <b>InputOffset</b> member of <a href="/windows/desktop/api/tdh/ns-tdh-event_map_entry">EVENT_MAP_ENTRY</a> to access the map value. For possible values, see the <a href="/windows/desktop/api/tdh/ne-tdh-map_valuetype">MAP_VALUETYPE</a> enumeration.

### -field FormatStringOffset

If the value of <b>Flag</b> is EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP, use this offset to access the null-terminated Unicode string that contains the value of the <b>format</b> attribute of the <a href="/windows/desktop/WES/eventmanifestschema-patternmaptype-complextype">patternMap</a> element. The offset is from the beginning of this structure.  

The EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP also indicates that you use the <b>InputOffset</b> member of <a href="/windows/desktop/api/tdh/ns-tdh-event_map_entry">EVENT_MAP_ENTRY</a> to access the map value.

### -field MapEntryArray

 Array of map entries. For details, see the <a href="/windows/desktop/api/tdh/ns-tdh-event_map_entry">EVENT_MAP_ENTRY</a> structure.

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhgeteventmapinformation">TdhGetEventMapInformation</a>