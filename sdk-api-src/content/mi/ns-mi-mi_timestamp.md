---
UID: NS:mi._MI_Timestamp
title: MI_Timestamp (mi.h)
description: MI_Timestamp specifies a timestamp or a specific point in time.
helpviewer_keywords: ["MI_Timestamp","MI_Timestamp structure [Windows Management Infrastructure (MI)]","mi/MI_Timestamp","wmi._mi_timestamp","wmi_v2.mi_timestamp"]
old-location: wmi_v2\mi_timestamp.htm
tech.root: wmi_v2
ms.assetid: f06f1b0e-d21c-4b60-8099-222a1582fde1
ms.date: 12/05/2018
ms.keywords: MI_Timestamp, MI_Timestamp structure [Windows Management Infrastructure (MI)], mi/MI_Timestamp, wmi._mi_timestamp, wmi_v2.mi_timestamp
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
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
req.typenames: MI_Timestamp
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_Timestamp
 - mi/_MI_Timestamp
 - MI_Timestamp
 - mi/MI_Timestamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Timestamp
---

# MI_Timestamp structure


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

