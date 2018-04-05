---
UID: NS:dhcpsapi._DATE_TIME
title: "_DATE_TIME"
author: windows-driver-content
description: The DATE_TIME structure defines a 64-bit integer value that contains a date/time, expressed as the number of ticks (100-nanosecond increments) since 12:00 midnight, January 1, 1 C.E. in the Gregorian calendar.
old-location: dhcp\date_time.htm
old-project: DHCP
ms.assetid: 2aca69b1-b7e5-4fda-b706-ed659d86cbd5
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*LPDATE_TIME, *PDATE_TIME, DATE_TIME, DATE_TIME structure [DHCP], LPDATE_TIME, LPDATE_TIME structure pointer [DHCP], _DATE_TIME, dhcp.date_time, dhcpsapi/LPDATE_TIME, dhcpsapi/_DATE_TIME"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: DATE_TIME, *PDATE_TIME, *LPDATE_TIME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DATE_TIME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DATE_TIME structure


## -description


The <b>DATE_TIME</b> structure defines a 64-bit integer value that contains  a date/time, expressed as the number of ticks (100-nanosecond increments) since 12:00 midnight, January 1, 1 C.E. in the Gregorian calendar. 


## -struct-fields




### -field dwLowDateTime

Specifies the lower 32 bits of the time value.


### -field dwHighDateTime

Specifies the upper 32 bits of the time value.


## -see-also




<a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">DHCP_CLIENT_INFO</a>
 

 

