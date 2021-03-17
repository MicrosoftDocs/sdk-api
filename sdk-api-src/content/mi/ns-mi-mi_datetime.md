---
UID: NS:mi._MI_Datetime
title: MI_Datetime (mi.h)
description: Represents a union of MI_Timestamp and MI_Interval.
helpviewer_keywords: ["MI_Datetime","MI_Datetime structure [Windows Management Infrastructure (MI)]","mi/MI_Datetime","wmi._mi_datetime","wmi_v2.mi_datetime"]
old-location: wmi_v2\mi_datetime.htm
tech.root: wmi_v2
ms.assetid: 2f7d857f-5115-40a2-84d9-a4429d935de1
ms.date: 12/05/2018
ms.keywords: MI_Datetime, MI_Datetime structure [Windows Management Infrastructure (MI)], mi/MI_Datetime, wmi._mi_datetime, wmi_v2.mi_datetime
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
req.typenames: MI_Datetime
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_Datetime
 - mi/_MI_Datetime
 - MI_Datetime
 - mi/MI_Datetime
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
 - MI_Datetime
---

# MI_Datetime structure


## -description

Represents a union of <a href="/windows/desktop/api/mi/ns-mi-mi_timestamp">MI_Timestamp</a> and <a href="/windows/desktop/api/mi/ns-mi-mi_interval">MI_Interval</a>.

## -struct-fields

### -field isTimestamp

If <b>isTimestamp</b> is nonzero, timestamp is used.  If <b>isTimestamp</b> is 0, interval is used.

### -field u

### -field u.timestamp

If <b>isTimestamp</b> is nonzero, <b>MI_Datetime</b> is used to represent an absolute date/time.

### -field u.interval

If <b>isTimestamp</b> is nonzero,  <b>MI_Datetime</b> is used to represent a relative date/time from when it is needed.