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

# _MI_Timestamp structure


## -description


<b>MI_Timestamp</b> specifies a timestamp or a specific point in time.


## -struct-fields




### -field year

A four digit number representing the year in the form yyyy.


### -field month

A two digit number representing the month in the form mm. (01-12)


### -field day

A two digit number representing the day of the month in the form dd. (01-31)


### -field hour

A two digit number representing the hour on a 24-hour clock in the form hh. (00-23)


### -field minute

A two digit number representing minutes in the form mm. (00-59)


### -field second

A two digit number representing seconds in the form ss. (00-59)


### -field microseconds

A six digit number in the form mmmmmm representing the microseconds. (000000-999999)


### -field utc

The offset from Coordinated Universal Time in minutes. Timezones west of Greenwich use negative numbers while timezones east of Greenwich use positive numbers.

