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

# _TIME_OF_DAY_INFO structure


## -description


The
				<b>TIME_OF_DAY_INFO</b> structure contains information about the time of day from a remote server.


## -struct-fields




### -field tod_elapsedt

Type: <b>DWORD</b>

The number of seconds since 00:00:00, January 1, 1970, GMT.


### -field tod_msecs

Type: <b>DWORD</b>

The number of milliseconds from an arbitrary starting point (system reset). 




Typically, this member is read twice, once when the process begins and again at the end. To determine the elapsed time between the process's start and finish, you can subtract the first value from the second.


### -field tod_hours

Type: <b>DWORD</b>

The current hour. Valid values are 0 through 23.


### -field tod_mins

Type: <b>DWORD</b>

The current minute. Valid values are 0 through 59.


### -field tod_secs

Type: <b>DWORD</b>

The current second. Valid values are 0 through 59.


### -field tod_hunds

Type: <b>DWORD</b>

The current hundredth second (0.01 second). Valid values are 0 through 99.


### -field tod_timezone

Type: <b>LONG</b>

The time zone of the server. This value is calculated, in minutes, from Greenwich Mean Time (GMT). For time zones west of Greenwich, the value is positive; for time zones east of Greenwich, the value is negative. A value of –1 indicates that the time zone is undefined.


### -field tod_tinterval

Type: <b>DWORD</b>

The time interval for each tick of the clock. Each integral integer represents one ten-thousandth second (0.0001 second).


### -field tod_day

Type: <b>DWORD</b>

The day of the month. Valid values are 1 through 31.


### -field tod_month

Type: <b>DWORD</b>

The month of the year. Valid values are 1 through 12.


### -field tod_year

Type: <b>DWORD</b>

The year.


### -field tod_weekday

Type: <b>DWORD</b>

The day of the week. Valid values are 0 through 6, where 0 is Sunday, 1 is Monday, and so on.


## -see-also




<a href="https://msdn.microsoft.com/5a935e09-f188-4ee1-b998-c67488475baa">NetRemoteTOD</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/e925d6d1-9347-4074-a12e-175b2115e71e">Remote Utility functions</a>
 

 

