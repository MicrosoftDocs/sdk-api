---
UID: NS:tdh._EVENT_MAP_INFO
title: "_EVENT_MAP_INFO"
author: windows-driver-content
description: Defines the metadata about the event map.
old-location: etw\event_map_info_struct.htm
old-project: ETW
ms.assetid: dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*PEVENT_MAP_INFO, EVENT_MAP_INFO, EVENT_MAP_INFO structure [ETW], _EVENT_MAP_INFO, etw.event_map_info_struct, tdh.event_map_info_struct, tdh/EVENT_MAP_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: EVENT_MAP_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tdh.h
api_name:
-	EVENT_MAP_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _EVENT_MAP_INFO structure


## -description



		Defines the metadata about the event map.


## -struct-fields




### -field NameOffset

Offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the event map.


### -field Flag

Indicates if the map is a value map, bitmap, or pattern map. This member can contain one or more flag values. For possible values, see the <a href="https://msdn.microsoft.com/3fc6935a-328a-4df3-8c2f-cd634d94ca16">MAP_FLAGS</a> enumeration.


### -field EntryCount

Number of map entries in <b>MapEntryArray</b>.


### -field MapEntryValueType

 
		Determines if you use the <b>Value</b> member or <b>InputOffset</b> member of <a href="https://msdn.microsoft.com/e5b12f7a-4a00-41a0-90df-7d1317d63a4a">EVENT_MAP_ENTRY</a> to access the map value. For possible values, see the <a href="https://msdn.microsoft.com/a17e5214-29d3-465f-9785-0cc8965a42c9">MAP_VALUETYPE</a> enumeration.


### -field FormatStringOffset

If the value of <b>Flag</b> is EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP, use this offset to access the null-terminated Unicode string that contains the value of the <b>format</b> attribute of the <a href="https://msdn.microsoft.com/184b6aeb-a554-4a92-b19e-1849c711d33b">patternMap</a> element. The offset is from the beginning of this structure.  

The EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP also indicates that you use the <b>InputOffset</b> member of <a href="https://msdn.microsoft.com/e5b12f7a-4a00-41a0-90df-7d1317d63a4a">EVENT_MAP_ENTRY</a> to access the map value.


### -field MapEntryArray

 Array of map entries. For details, see the <a href="https://msdn.microsoft.com/e5b12f7a-4a00-41a0-90df-7d1317d63a4a">EVENT_MAP_ENTRY</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/2625b65c-7f9e-4a87-85c6-d16857ef4987">TdhGetEventMapInformation</a>
 

 

