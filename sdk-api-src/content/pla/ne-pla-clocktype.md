---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0005
title: ClockType (pla.h)
description: Defines the clock resolution to use when tracing events.
helpviewer_keywords: ["ClockType","ClockType enumeration [PLA]","base.clocktype","pla.clocktype","pla/ClockType","pla/plaCycle","pla/plaPerformance","pla/plaSystem","pla/plaTimeStamp","plaCycle","plaPerformance","plaSystem","plaTimeStamp"]
old-location: pla\clocktype.htm
tech.root: PLA
ms.assetid: e255d486-2f1f-4a3d-a8a5-1c997d61a073
ms.date: 12/05/2018
ms.keywords: ClockType, ClockType enumeration [PLA], base.clocktype, pla.clocktype, pla/ClockType, pla/plaCycle, pla/plaPerformance, pla/plaSystem, pla/plaTimeStamp, plaCycle, plaPerformance, plaSystem, plaTimeStamp
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: ClockType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_pla_0001_0043_0005
 - pla/__MIDL___MIDL_itf_pla_0001_0043_0005
 - ClockType
 - pla/ClockType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - ClockType
---

# ClockType enumeration


## -description

Defines the clock resolution to use when tracing events.

## -enum-fields

### -field plaTimeStamp:0

Use the raw (unconverted) time stamp.

### -field plaPerformance:1

Query performance counter. This counter provides a high-resolution (100 nanoseconds) time stamp but is more resource-intensive to retrieve than  system time.

### -field plaSystem:2

System time. The system time provides a low-resolution (10 milliseconds) time stamp but is less resource-intensive to retrieve than the query performance counter.

### -field plaCycle:3

CPU cycle counter. The CPU counter provides the highest resolution time stamp and is the least resource-intensive to retrieve. However, the CPU counter is unreliable and should not be used in production.

## -remarks

For details, see the <b>ClientContext</b> member of the <a href="/windows/desktop/ETW/wnode-header">WNODE_HEADER</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-itracedatacollector-get_clocktype">ITraceDataCollector::ClockType</a>
