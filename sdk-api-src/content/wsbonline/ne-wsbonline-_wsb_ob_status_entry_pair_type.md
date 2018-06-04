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

# _WSB_OB_STATUS_ENTRY_PAIR_TYPE enumeration


## -description


The <b>WSB_OB_STATUS_ENTRY_PAIR_TYPE</b> enumeration indicates the type of the parameter value contained in the <a href="https://msdn.microsoft.com/FA92796E-7C26-4FD0-8AC2-F84F8F5E5A6C">WSB_OB_STATUS_ENTRY_VALUE_TYPE_PAIR</a> structure.


## -enum-fields




### -field WSB_OB_ET_UNDEFINED

The value type is undefined.


### -field WSB_OB_ET_STRING

The value type is string.


### -field WSB_OB_ET_NUMBER

The value type is integer.


### -field WSB_OB_ET_DATETIME

The value type is datetime which represents an instant in time, typically expressed as a date and time of day. All time-related values are specified in Coordinated Universal Time (UTC) format.


### -field WSB_OB_ET_TIME

The value type is time. All time-related values are specified in UTC format.


### -field WSB_OB_ET_SIZE

The value type is size.


### -field WSB_OB_ET_MAX

The maximum enumeration value for this enumeration.


## -see-also




<a href="https://msdn.microsoft.com/27CDCBA3-9BBB-4A94-8F4E-57842C31F6CE">Cloud Backup Provider API Enumerations</a>
 

 

