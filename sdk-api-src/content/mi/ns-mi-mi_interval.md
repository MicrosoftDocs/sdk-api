---
UID: NS:mi._MI_Interval
title: MI_Interval (mi.h)
description: MI_Interval represents an interval of time.
helpviewer_keywords: ["MI_Interval","MI_Interval structure [Windows Management Infrastructure (MI)]","mi/MI_Interval","wmi._mi_interval","wmi_v2.mi_interval"]
old-location: wmi_v2\mi_interval.htm
tech.root: wmi_v2
ms.assetid: b6bf3d47-c292-4140-8bc6-f15ad8a8019f
ms.date: 12/05/2018
ms.keywords: MI_Interval, MI_Interval structure [Windows Management Infrastructure (MI)], mi/MI_Interval, wmi._mi_interval, wmi_v2.mi_interval
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
req.typenames: MI_Interval
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_Interval
 - mi/_MI_Interval
 - MI_Interval
 - mi/MI_Interval
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
 - MI_Interval
---

# MI_Interval structure


## -description

<b>MI_Interval</b> represents an interval of time.

## -struct-fields

### -field days

The number of days in the interval. (0-99999999)

### -field hours

The remaining number of hours in the interval. (0-23)

### -field minutes

The remaining number of minutes in the interval. (0-59)

### -field seconds

The remaining number of seconds in the interval. (0-59)

### -field microseconds

The remaining number of microseconds in the interval. (0-999999)

### -field __padding1

Reserved. The <b>MI_Interval</b> structure is padded to have the same size as <a href="/windows/desktop/api/mi/ns-mi-mi_timestamp">MI_Timestamp</a>.

### -field __padding2

Reserved. The <b>MI_Interval</b> structure is padded to have the same size as <a href="/windows/desktop/api/mi/ns-mi-mi_timestamp">MI_Timestamp</a>.

### -field __padding3

Reserved. The <b>MI_Interval</b> structure is padded to have the same size as <a href="/windows/desktop/api/mi/ns-mi-mi_timestamp">MI_Timestamp</a>.