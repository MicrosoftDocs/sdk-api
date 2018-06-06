---
UID: NS:wsdxml._WSD_DATETIME
title: "_WSD_DATETIME"
author: windows-sdk-content
description: Represents a timestamp.
old-location: ncd\wsd_datetime_struct.htm
old-project: WsdApi
ms.assetid: ec42d69c-133a-4e76-bbbe-0e6978f4723a
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSD_DATETIME, WSD_DATETIME structure, _WSD_DATETIME, ncd.wsd_datetime_struct, wsdxml/WSD_DATETIME
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdxml.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdXml.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_DATETIME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdXml.h
api_name:
 - WSD_DATETIME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_DATETIME structure


## -description


Represents a timestamp.


## -struct-fields




### -field isPositive

<b>TRUE</b> if <i>year</i> value is positive.


### -field year

Year value (for example, 2005). This number is a value between 0 and max(ULONG).


### -field month

One-based month value (1 = January, through 12 = December).


### -field day

One-based day of the month value (1-31). 


### -field hour

Zero-based hour value (0 through 23). <i>hour</i>=24 is only allowed if both <i>minute</i> and <i>second</i> are 0.


### -field minute

Zero-based minute value (0 through 59). 


### -field second

Zero-based second value (0 through 59). 


### -field millisecond

Millisecond value (0-999). When this structure is converted to XML, the millisecond value is expressed as a fraction of a second in decimal form. For example, if <b>millisecond</b> has a value of 9, then the XML output will be 0.009. 


### -field TZIsLocal

<b>TRUE</b> if date and time are based on the local time zone, <b>FALSE</b> if UTC + offset.


### -field TZIsPositive

<b>TRUE</b> if time zone offset specified by  <i>TZHour</i> and <i>TZMinute</i> is positive relative to UTC, <b>FALSE</b> if offset is negative. Not valid if <i>TZIsLocal</i> is <b>TRUE</b>.


### -field TZHour

Time zone offset relative to UTC (0-13). <i>TZhour</i>=14 is allowed if <i>TZMinute</i> is 0. Not valid if <i>TZIsLocal</i> is <b>TRUE</b>.


### -field TZMinute

Time zone offset relative to UTC (0-59). Not valid if <i>TZIsLocal</i> is <b>TRUE</b>.

