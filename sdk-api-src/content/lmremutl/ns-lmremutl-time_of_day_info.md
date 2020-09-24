---
UID: NS:lmremutl._TIME_OF_DAY_INFO
title: TIME_OF_DAY_INFO (lmremutl.h)
description: The TIME_OF_DAY_INFO structure contains information about the time of day from a remote server.
helpviewer_keywords: ["*LPTIME_OF_DAY_INFO","*PTIME_OF_DAY_INFO","LPTIME_OF_DAY_INFO","LPTIME_OF_DAY_INFO structure pointer [Network Management]","PTIME_OF_DAY_INFO","PTIME_OF_DAY_INFO structure pointer [Network Management]","TIME_OF_DAY_INFO","TIME_OF_DAY_INFO structure [Network Management]","_win32_time_of_day_info_str","lmremutl/LPTIME_OF_DAY_INFO","lmremutl/PTIME_OF_DAY_INFO","lmremutl/TIME_OF_DAY_INFO","netmgmt.time_of_day_info_str"]
old-location: netmgmt\time_of_day_info_str.htm
tech.root: NetMgmt
ms.assetid: bf89f071-5c04-40c2-a7b7-4e59fc9eaa02
ms.date: 12/05/2018
ms.keywords: '*LPTIME_OF_DAY_INFO, *PTIME_OF_DAY_INFO, LPTIME_OF_DAY_INFO, LPTIME_OF_DAY_INFO structure pointer [Network Management], PTIME_OF_DAY_INFO, PTIME_OF_DAY_INFO structure pointer [Network Management], TIME_OF_DAY_INFO, TIME_OF_DAY_INFO structure [Network Management], _win32_time_of_day_info_str, lmremutl/LPTIME_OF_DAY_INFO, lmremutl/PTIME_OF_DAY_INFO, lmremutl/TIME_OF_DAY_INFO, netmgmt.time_of_day_info_str'
req.header: lmremutl.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: TIME_OF_DAY_INFO, *PTIME_OF_DAY_INFO, *LPTIME_OF_DAY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TIME_OF_DAY_INFO
 - lmremutl/_TIME_OF_DAY_INFO
 - PTIME_OF_DAY_INFO
 - lmremutl/PTIME_OF_DAY_INFO
 - TIME_OF_DAY_INFO
 - lmremutl/TIME_OF_DAY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmremutl.h
api_name:
 - TIME_OF_DAY_INFO
---

# TIME_OF_DAY_INFO structure


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

<a href="/windows/desktop/api/lmremutl/nf-lmremutl-netremotetod">NetRemoteTOD</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/remote-utility-functions">Remote Utility functions</a>