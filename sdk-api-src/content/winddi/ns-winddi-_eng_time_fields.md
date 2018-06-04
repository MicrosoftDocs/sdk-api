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

# _ENG_TIME_FIELDS structure


## -description


The ENG_TIME_FIELDS structure is used by the  <a href="https://msdn.microsoft.com/library/windows/hardware/ff564990">EngQueryLocalTime</a> function to return the local time. 


## -struct-fields




### -field usYear

Specifies the current calendar year. The range is [1601,...].


### -field usMonth

Specifies the current calendar month. The range is [1,12].


### -field usDay

Specifies the current calendar day. The range is [1,31].


### -field usHour

Specifies the current hour. The range is [0,23].


### -field usMinute

Specifies the current minute. The range is [0,59].


### -field usSecond

Specifies the current second. The range is [0,59].


### -field usMilliseconds

Specifies the current millisecond. The range is [0,999].


### -field usWeekday

Specifies the current day. The range is [0,6], where 0 is Sunday and 6 is Saturday.


## -remarks



The driver is responsible for allocating the ENG_TIME_FIELDS structure and passing its pointer to <b>EngQueryLocalTime</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564990">EngQueryLocalTime</a>
 

 

