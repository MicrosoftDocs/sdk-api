---
UID: NE:tdh._MAP_VALUETYPE
title: "_MAP_VALUETYPE"
author: windows-sdk-content
description: Defines if the value map value is in a ULONG data type or a string.
old-location: etw\map_valuetype_enum.htm
old-project: ETW
ms.assetid: a17e5214-29d3-465f-9785-0cc8965a42c9
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: EVENTMAP_ENTRY_VALUETYPE_STRING, EVENTMAP_ENTRY_VALUETYPE_ULONG, MAP_VALUETYPE, MAP_VALUETYPE enumeration [ETW], _MAP_VALUETYPE, etw.map_valuetype_enum, tdh.map_valuetype_enum, tdh/EVENTMAP_ENTRY_VALUETYPE_STRING, tdh/EVENTMAP_ENTRY_VALUETYPE_ULONG, tdh/MAP_VALUETYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: MAP_VALUETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tdh.h
api_name:
-	MAP_VALUETYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _MAP_VALUETYPE enumeration


## -description



		Defines if the value map value is in a ULONG data type or a string.


## -enum-fields




### -field EVENTMAP_ENTRY_VALUETYPE_ULONG

Use the <b>Value</b> member of <a href="https://msdn.microsoft.com/e5b12f7a-4a00-41a0-90df-7d1317d63a4a">EVENT_MAP_ENTRY</a> to access the map value. 


### -field EVENTMAP_ENTRY_VALUETYPE_STRING

Use the <b>InputOffset</b> member of <a href="https://msdn.microsoft.com/e5b12f7a-4a00-41a0-90df-7d1317d63a4a">EVENT_MAP_ENTRY</a> to access the map value.


## -see-also




<a href="https://msdn.microsoft.com/dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98">EVENT_MAP_INFO</a>
 

 

