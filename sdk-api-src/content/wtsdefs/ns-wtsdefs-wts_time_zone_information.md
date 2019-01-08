---
UID: NS:wtsdefs._WTS_TIME_ZONE_INFORMATION
title: WTS_TIME_ZONE_INFORMATION
author: windows-sdk-content
description: Contains client time zone information.
old-location: termserv\wts_time_zone_information.htm
tech.root: termserv
ms.assetid: 7d0e75b1-0a9b-47b1-8bf7-192966e3d19a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWTS_TIME_ZONE_INFORMATION, PWRDS_TIME_ZONE_INFORMATION, PWRDS_TIME_ZONE_INFORMATION structure pointer [Remote Desktop Services], PWTS_TIME_ZONE_INFORMATION, PWTS_TIME_ZONE_INFORMATION structure pointer [Remote Desktop Services], WRDS_TIME_ZONE_INFORMATION, WRDS_TIME_ZONE_INFORMATION structure [Remote Desktop Services], WTS_TIME_ZONE_INFORMATION, WTS_TIME_ZONE_INFORMATION structure [Remote Desktop Services], termserv.wts_time_zone_information, wtsdefs/PWRDS_TIME_ZONE_INFORMATION, wtsdefs/PWTS_TIME_ZONE_INFORMATION, wtsdefs/WRDS_TIME_ZONE_INFORMATION, wtsdefs/WTS_TIME_ZONE_INFORMATION"
ms.topic: struct
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - Wtsdefs.h
api_name:
 - WTS_TIME_ZONE_INFORMATION
product: Windows
targetos: Windows
req.typenames: WTS_TIME_ZONE_INFORMATION, *PWTS_TIME_ZONE_INFORMATION
req.redist: 
---

# WTS_TIME_ZONE_INFORMATION structure


## -description


Contains client time zone information.


## -struct-fields




### -field Bias

An integer that contains the bias for local time translation.  Bias is the difference, in minutes, between Coordinated Universal Time (Greenwich Mean Time) and local time.


### -field StandardName

A string that contains a descriptive name for standard time on the client. Examples include "Pacific Standard Time".


### -field StandardDate

A <a href="https://msdn.microsoft.com/3d123666-c13c-4061-9c03-a84cc3ab2a51">WTS_SYSTEMTIME</a> structure that contains the date and local time when the transition from daylight saving time to standard time occurs on the client. If this field is specified, the <b>DaylightDate</b> member should also be specified.


### -field StandardBias

An integer that defines the bias, in minutes, to be used during local time translations that occur during standard time. This value is added to the value of the <b>Bias</b> member to form the bias used during standard time. In most time zones, the value of this field is zero.


### -field DaylightName

A string that contains a descriptive name for daylight saving time on the client. Examples include "Pacific Daylight Time".


### -field DaylightDate

A <a href="https://msdn.microsoft.com/3d123666-c13c-4061-9c03-a84cc3ab2a51">WTS_SYSTEMTIME</a> structure that contains the date and local time when the transition from standard time to daylight saving time occurs on the client. If this field is specified, the <b>StandardDate</b> member should also be specified.


### -field DaylightBias

An integer that defines the bias, in minutes, to be used during local time translations that occur during daylight saving time. This value is added to the value of the <b>Bias</b> member to form the bias used during daylight saving time. In most time zones, the value of this field is 60.

