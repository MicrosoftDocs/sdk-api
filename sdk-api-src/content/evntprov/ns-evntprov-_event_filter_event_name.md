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

# _EVENT_FILTER_EVENT_NAME structure


## -description


The <b>EVENT_FILTER_EVENT_NAME</b> structure defines event IDs used in an <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure for an  event name or stalk walk name filter. 

This filter will only be applied to events that are otherwise enabled
on the logging session, via level/keyword in the enable call.


## -struct-fields




### -field MatchAnyKeyword

Bitmask of keywords that determine the category of events to filter on.


### -field MatchAllKeyword

This bitmask is optional. This mask further restricts the category of events that you want to filter on. If the event's keyword meets the <b>MatchAnyKeyword</b> condition, the provider will filter the event only if all of the bits in this mask exist in the event's keyword. This mask is not used if <b>MatchAnyKeyword</b> is zero.


### -field Level

Defines the severity level of the event to filter on.


### -field FilterIn

<b>True</b> to filter the events matching the provided names in; <b>false</b> to filter them out.

When used for the <b>EVENT_FILTER_TYPE_STACKWALK_NAME</b>
filter type, the filtered in events will have stacks collected for them.


### -field NameCount

The number of names in the <b>Names</b> member.


### -field Names

An <b>NameCount</b> long array of null-terminated, UTF-8
event names.


## -remarks







