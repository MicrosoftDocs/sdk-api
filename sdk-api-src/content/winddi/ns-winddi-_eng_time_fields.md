---
UID: NS:winddi._ENG_TIME_FIELDS
title: "_ENG_TIME_FIELDS"
author: windows-sdk-content
description: The ENG_TIME_FIELDS structure is used by the EngQueryLocalTime function to return the local time.
old-location: display\eng_time_fields.htm
tech.root: Display
ms.assetid: 482e1d15-d499-4ed2-87e7-760f03a454b5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PENG_TIME_FIELDS, ENG_TIME_FIELDS, ENG_TIME_FIELDS structure [Display Devices], PENG_TIME_FIELDS, PENG_TIME_FIELDS structure pointer [Display Devices], _ENG_TIME_FIELDS, display.eng_time_fields, grstrcts_3611274f-4217-48c5-af9d-9470df8a39e8.xml, winddi/ENG_TIME_FIELDS, winddi/PENG_TIME_FIELDS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - ENG_TIME_FIELDS
product: Windows
targetos: Windows
req.typenames: ENG_TIME_FIELDS, *PENG_TIME_FIELDS
req.redist: 
---

# _ENG_TIME_FIELDS structure


## -description


The ENG_TIME_FIELDS structure is used by the  <a href="https://msdn.microsoft.com/826993fc-7cf2-4747-a0d9-086e5d7310b6">EngQueryLocalTime</a> function to return the local time. 


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




<a href="https://msdn.microsoft.com/826993fc-7cf2-4747-a0d9-086e5d7310b6">EngQueryLocalTime</a>
 

 

