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

# _WTS_SYSTEMTIME structure


## -description


Specifies date and time information for transitions between standard time and daylight saving time.


## -struct-fields




### -field wYear

The year from 1601 to 30827.


### -field wMonth

The month when transition from standard to daylight saving time occurs. This can be one of the following values.



#### 1

January



#### 2

February



#### 3

March



#### 4

April



#### 5

May



#### 6

June



#### 7

July



#### 8

August



#### 9

September



#### 10

October



#### 11

November



#### 12

December


### -field wDayOfWeek

The day of the week when the transition occurs. This can be one of the following values.



#### 0

Sunday



#### 1

Monday



#### 2

Tuesday



#### 3

Wednesday



#### 4

Thursday



#### 5

Friday



#### 6

Saturday


### -field wDay

The day of the month when the transition occurs.


### -field wHour

The hour when the transition occurs.


### -field wMinute

The minute when the transition occurs.


### -field wSecond

The second when the transition occurs.


### -field wMilliseconds

The millisecond when the transition occurs.

