---
UID: NS:tdh._EVENT_MAP_ENTRY
title: "_EVENT_MAP_ENTRY"
author: windows-sdk-content
description: Defines a single value map entry.
old-location: etw\event_map_entry_struct.htm
tech.root: etw
ms.assetid: e5b12f7a-4a00-41a0-90df-7d1317d63a4a
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: "*PEVENT_MAP_ENTRY, EVENT_MAP_ENTRY, EVENT_MAP_ENTRY structure [ETW], EVENT_MAP_ENTRY,*PEVENT_MAP_ENTRY, EVENT_MAP_ENTRY,*PEVENT_MAP_ENTRY structure [ETW], _EVENT_MAP_ENTRY, etw.event_map_entry_struct, tdh.event_map_entry_struct, tdh/EVENT_MAP_ENTRY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - EVENT_MAP_ENTRY, *PEVENT_MAP_ENTRY
product: Windows
targetos: Windows
req.typenames: EVENT_MAP_ENTRY
req.redist: 
---

# _EVENT_MAP_ENTRY structure


## -description


Defines a single value map entry. 


## -struct-fields




### -field OutputOffset

Offset from the beginning of the <a href="https://msdn.microsoft.com/dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98">EVENT_MAP_INFO</a> structure to a null-terminated Unicode string that contains the string associated with the map value in <b>Value</b> or <b>InputOffset</b>.


### -field Value

If the <b>MapEntryValueType</b> member of <a href="https://msdn.microsoft.com/dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98">EVENT_MAP_INFO</a>  is EVENTMAP_ENTRY_VALUETYPE_ULONG, use this member to access the map value.


### -field InputOffset

Offset from the beginning of the <a href="https://msdn.microsoft.com/dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98">EVENT_MAP_INFO</a> structure to the null-terminated Unicode string that contains the map value.

The offset is used for pattern maps and WMI value maps that map strings to strings. 


## -remarks



For maps defined in a manifest, the string will contain a space at the end of the string. For example, if the value is mapped to "Monday" in the manifest, the string is returned as "Monday ".




## -see-also




<a href="https://msdn.microsoft.com/dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98">EVENT_MAP_INFO</a>
 

 

