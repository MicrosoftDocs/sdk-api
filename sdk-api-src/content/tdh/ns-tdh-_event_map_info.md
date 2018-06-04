---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

