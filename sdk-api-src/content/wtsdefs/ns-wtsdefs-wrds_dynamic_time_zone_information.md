---
UID: NS:wtsdefs._WRDS_DYNAMIC_TIME_ZONE_INFORMATION
title: WRDS_DYNAMIC_TIME_ZONE_INFORMATION (wtsdefs.h)
description: Contains dynamic time zone information.
helpviewer_keywords: ["*PWRDS_DYNAMIC_TIME_ZONE_INFORMATION","PWRDS_DYNAMIC_TIME_ZONE_INFORMATION","PWRDS_DYNAMIC_TIME_ZONE_INFORMATION structure pointer [Remote Desktop Services]","WRDS_DYNAMIC_TIME_ZONE_INFORMATION","WRDS_DYNAMIC_TIME_ZONE_INFORMATION structure [Remote Desktop Services]","termserv.wrds_dynamic_time_zone_information","wtsdefs/PWRDS_DYNAMIC_TIME_ZONE_INFORMATION","wtsdefs/WRDS_DYNAMIC_TIME_ZONE_INFORMATION"]
old-location: termserv\wrds_dynamic_time_zone_information.htm
tech.root: TermServ
ms.assetid: D529B7BB-380F-462E-99B8-E565B9636D97
ms.date: 12/05/2018
ms.keywords: '*PWRDS_DYNAMIC_TIME_ZONE_INFORMATION, PWRDS_DYNAMIC_TIME_ZONE_INFORMATION, PWRDS_DYNAMIC_TIME_ZONE_INFORMATION structure pointer [Remote Desktop Services], WRDS_DYNAMIC_TIME_ZONE_INFORMATION, WRDS_DYNAMIC_TIME_ZONE_INFORMATION structure [Remote Desktop Services], termserv.wrds_dynamic_time_zone_information, wtsdefs/PWRDS_DYNAMIC_TIME_ZONE_INFORMATION, wtsdefs/WRDS_DYNAMIC_TIME_ZONE_INFORMATION'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: WRDS_DYNAMIC_TIME_ZONE_INFORMATION, *PWRDS_DYNAMIC_TIME_ZONE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WRDS_DYNAMIC_TIME_ZONE_INFORMATION
 - wtsdefs/_WRDS_DYNAMIC_TIME_ZONE_INFORMATION
 - PWRDS_DYNAMIC_TIME_ZONE_INFORMATION
 - wtsdefs/PWRDS_DYNAMIC_TIME_ZONE_INFORMATION
 - WRDS_DYNAMIC_TIME_ZONE_INFORMATION
 - wtsdefs/WRDS_DYNAMIC_TIME_ZONE_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WRDS_DYNAMIC_TIME_ZONE_INFORMATION
---

# WRDS_DYNAMIC_TIME_ZONE_INFORMATION structure


## -description

Contains dynamic time zone information.

## -struct-fields

### -field Bias

An integer that contains the bias for local time translation.  Bias is the difference, in minutes, between Coordinated Universal Time (Greenwich Mean Time) and local time.

### -field StandardName

A string that contains a descriptive name for standard time on the client. Examples include "Pacific Standard Time".

### -field StandardDate

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_systemtime">WTS_SYSTEMTIME</a> structure that contains the date and local time when the transition from daylight saving time to standard time occurs on the client. If this field is specified, the <b>DaylightDate</b> member should also be specified.

### -field StandardBias

An integer that defines the bias, in minutes, to be used during local time translations that occur during standard time. This value is added to the value of the <b>Bias</b> member to form the bias used during standard time. In most time zones, the value of this field is zero.

### -field DaylightName

A string that contains a descriptive name for daylight saving time on the client. Examples include "Pacific Daylight Time".

### -field DaylightDate

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_systemtime">WTS_SYSTEMTIME</a> structure that contains the date and local time when the transition from standard time to daylight saving time occurs on the client. If this field is specified, the <b>StandardDate</b> member should also be specified.

### -field DaylightBias

An integer that defines the bias, in minutes, to be used during local time translations that occur during daylight saving time. This value is added to the value of the <b>Bias</b> member to form the bias used during daylight saving time. In most time zones, the value of this field is 60.

### -field TimeZoneKeyName

Key name for the TimeZone information.

### -field DynamicDaylightTimeDisabled

Whether DynamicDaylightTime is disabled.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>



<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty">QueryProperty</a>