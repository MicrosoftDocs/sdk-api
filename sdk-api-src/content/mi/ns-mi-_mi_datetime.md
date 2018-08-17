---
UID: NS:mi._MI_Datetime
title: "_MI_Datetime"
author: windows-sdk-content
description: Represents a union of MI_Timestamp and MI_Interval.
old-location: wmi_v2\mi_datetime.htm
old-project: wmi_v2
ms.assetid: 2f7d857f-5115-40a2-84d9-a4429d935de1
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_Datetime, MI_Datetime structure [Windows Management Infrastructure (MI)], _MI_Datetime, mi/MI_Datetime, wmi._mi_datetime, wmi_v2.mi_datetime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
tech.root: 
req.typenames: MI_Datetime
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Datetime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_Datetime structure


## -description


Represents a union of <a href="https://msdn.microsoft.com/f06f1b0e-d21c-4b60-8099-222a1582fde1">MI_Timestamp</a> and <a href="https://msdn.microsoft.com/b6bf3d47-c292-4140-8bc6-f15ad8a8019f">MI_Interval</a>.


## -struct-fields




### -field isTimestamp

If <b>isTimestamp</b> is nonzero, timestamp is used.  If <b>isTimestamp</b> is 0, interval is used.


### -field u


### -field u.timestamp

If <b>isTimestamp</b> is nonzero, <b>MI_Datetime</b> is used to represent an absolute date/time.


### -field u.interval

If <b>isTimestamp</b> is nonzero,  <b>MI_Datetime</b> is used to represent a relative date/time from when it is needed.

