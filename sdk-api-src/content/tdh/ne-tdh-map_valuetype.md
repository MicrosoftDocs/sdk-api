---
UID: NE:tdh._MAP_VALUETYPE
title: MAP_VALUETYPE (tdh.h)
description: Defines if the value map value is in a ULONG data type or a string.
helpviewer_keywords: ["EVENTMAP_ENTRY_VALUETYPE_STRING","EVENTMAP_ENTRY_VALUETYPE_ULONG","MAP_VALUETYPE","MAP_VALUETYPE enumeration [ETW]","etw.map_valuetype_enum","tdh.map_valuetype_enum","tdh/EVENTMAP_ENTRY_VALUETYPE_STRING","tdh/EVENTMAP_ENTRY_VALUETYPE_ULONG","tdh/MAP_VALUETYPE"]
old-location: etw\map_valuetype_enum.htm
tech.root: ETW
ms.assetid: a17e5214-29d3-465f-9785-0cc8965a42c9
ms.date: 12/05/2018
ms.keywords: EVENTMAP_ENTRY_VALUETYPE_STRING, EVENTMAP_ENTRY_VALUETYPE_ULONG, MAP_VALUETYPE, MAP_VALUETYPE enumeration [ETW], etw.map_valuetype_enum, tdh.map_valuetype_enum, tdh/EVENTMAP_ENTRY_VALUETYPE_STRING, tdh/EVENTMAP_ENTRY_VALUETYPE_ULONG, tdh/MAP_VALUETYPE
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
req.typenames: MAP_VALUETYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MAP_VALUETYPE
 - tdh/_MAP_VALUETYPE
 - MAP_VALUETYPE
 - tdh/MAP_VALUETYPE
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
 - MAP_VALUETYPE
---

# MAP_VALUETYPE enumeration


## -description

Defines if the value map value is in a ULONG data type or a string.

## -enum-fields

### -field EVENTMAP_ENTRY_VALUETYPE_ULONG

Use the <b>Value</b> member of <a href="/windows/desktop/api/tdh/ns-tdh-event_map_entry">EVENT_MAP_ENTRY</a> to access the map value.

### -field EVENTMAP_ENTRY_VALUETYPE_STRING

Use the <b>InputOffset</b> member of <a href="/windows/desktop/api/tdh/ns-tdh-event_map_entry">EVENT_MAP_ENTRY</a> to access the map value.

## -see-also
<a href="/windows/desktop/api/tdh/ns-tdh-event_map_info">EVENT_MAP_INFO</a>