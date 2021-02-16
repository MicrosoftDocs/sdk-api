---
UID: NS:wtsdefs._WTS_SYSTEMTIME
title: WTS_SYSTEMTIME (wtsdefs.h)
description: Specifies date and time information for transitions between standard time and daylight saving time.
helpviewer_keywords: ["*PWTS_SYSTEMTIME","0","1","10","11","12","2","3","4","5","6","7","8","9","PWRDS_SYSTEMTIME","PWRDS_SYSTEMTIME structure [Remote Desktop Services]","PWTS_SYSTEMTIME","PWTS_SYSTEMTIME structure pointer [Remote Desktop Services]","WRDS_SYSTEMTIME","WRDS_SYSTEMTIME structure [Remote Desktop Services]","WTS_SYSTEMTIME","WTS_SYSTEMTIME structure [Remote Desktop Services]","termserv.wts_systemtime","wtsdefs/PWRDS_SYSTEMTIME","wtsdefs/PWTS_SYSTEMTIME","wtsdefs/WRDS_SYSTEMTIME","wtsdefs/WTS_SYSTEMTIME"]
old-location: termserv\wts_systemtime.htm
tech.root: TermServ
ms.assetid: 3d123666-c13c-4061-9c03-a84cc3ab2a51
ms.date: 12/05/2018
ms.keywords: '*PWTS_SYSTEMTIME, 0, 1, 10, 11, 12, 2, 3, 4, 5, 6, 7, 8, 9, PWRDS_SYSTEMTIME, PWRDS_SYSTEMTIME structure [Remote Desktop Services], PWTS_SYSTEMTIME, PWTS_SYSTEMTIME structure pointer [Remote Desktop Services], WRDS_SYSTEMTIME, WRDS_SYSTEMTIME structure [Remote Desktop Services], WTS_SYSTEMTIME, WTS_SYSTEMTIME structure [Remote Desktop Services], termserv.wts_systemtime, wtsdefs/PWRDS_SYSTEMTIME, wtsdefs/PWTS_SYSTEMTIME, wtsdefs/WRDS_SYSTEMTIME, wtsdefs/WTS_SYSTEMTIME'
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
targetos: Windows
req.typenames: WTS_SYSTEMTIME, *PWTS_SYSTEMTIME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_SYSTEMTIME
 - wtsdefs/_WTS_SYSTEMTIME
 - PWTS_SYSTEMTIME
 - wtsdefs/PWTS_SYSTEMTIME
 - WTS_SYSTEMTIME
 - wtsdefs/WTS_SYSTEMTIME
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
 - WTS_SYSTEMTIME
---

# WTS_SYSTEMTIME structure


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

