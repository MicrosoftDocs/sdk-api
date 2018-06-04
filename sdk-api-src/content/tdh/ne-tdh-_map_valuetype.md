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
 

 

