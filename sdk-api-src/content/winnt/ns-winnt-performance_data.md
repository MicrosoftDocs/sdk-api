---
UID: NS:winnt._PERFORMANCE_DATA
title: PERFORMANCE_DATA (winnt.h)
description: Contains the thread profiling and hardware counter data that you requested.
helpviewer_keywords: ["*PPERFORMANCE_DATA","PERFORMANCE_DATA","PERFORMANCE_DATA structure [Hardware Counter Profiling]","PPERFORMANCE_DATA","PPERFORMANCE_DATA structure pointer [Hardware Counter Profiling]","_PERFORMANCE_DATA","hcp.performance_data","winnt/PERFORMANCE_DATA","winnt/PPERFORMANCE_DATA"]
old-location: hcp\performance_data.htm
tech.root: hcp
ms.assetid: 468060cc-7b17-4ef4-8ae0-74d2bfcd5e4a
ms.date: 12/05/2018
ms.keywords: '*PPERFORMANCE_DATA, PERFORMANCE_DATA, PERFORMANCE_DATA structure [Hardware Counter Profiling], PPERFORMANCE_DATA, PPERFORMANCE_DATA structure pointer [Hardware Counter Profiling], _PERFORMANCE_DATA, hcp.performance_data, winnt/PERFORMANCE_DATA, winnt/PPERFORMANCE_DATA'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PERFORMANCE_DATA, *PPERFORMANCE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERFORMANCE_DATA
 - winnt/_PERFORMANCE_DATA
 - PPERFORMANCE_DATA
 - winnt/PPERFORMANCE_DATA
 - PERFORMANCE_DATA
 - winnt/PERFORMANCE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - PERFORMANCE_DATA
---

# PERFORMANCE_DATA structure


## -description

Contains the thread profiling and hardware counter data that you requested.

## -struct-fields

### -field Size

The size of this structure.

### -field Version

The version of this structure. Must be set to PERFORMANCE_DATA_VERSION.

### -field HwCountersCount

The number of array elements in the <b>HwCounters</b> array that contain hardware counter data. A value of 3 means that the array contains data for three hardware counters, not that elements 0 through 2 contain counter data.

### -field ContextSwitchCount

The number of context switches that occurred from the time profiling was enabled.

### -field WaitReasonBitMap

A bitmask that identifies the reasons for the context switches that occurred since the last time the data was read. For possible values, see the <b>KWAIT_REASON</b> enumeration (the enumeration is included in the Wdm.h file in the WDK).

### -field CycleTime

The cycle time of the thread (excludes the time spent interrupted) from the time profiling was enabled.

### -field RetryCount

The number of times that the read operation read the data to ensure a consistent snapshot of the data.

### -field Reserved

Reserved. Set to zero.

### -field HwCounters

An array of <a href="/windows/desktop/api/winnt/ns-winnt-hardware_counter_data">HARDWARE_COUNTER_DATA</a> structures that contain the counter values. The elements of the array that contain counter data relate directly to the bits set in the <i>HardwareCounters</i> bitmask that you specified when you called the <a href="/windows/desktop/api/winbase/nf-winbase-enablethreadprofiling">EnableThreadProfiling</a> function. For example, if you set bit 3 in the <i>HardwareCounters</i> bitmask, HwCounters[3] will contain the counter data for that counter.

## -remarks

You must initialize the <b>Size</b> and <b>Version</b> members before calling the <a href="/windows/desktop/api/winbase/nf-winbase-readthreadprofilingdata">ReadThreadProfilingData</a> function to read the profiling data.

The profile data contained in this structure depends on the data that you requested when you called the <a href="/windows/desktop/api/winbase/nf-winbase-readthreadprofilingdata">ReadThreadProfilingData</a> function. The following members are set when you specify the READ_THREAD_PROFILING_FLAG_DISPATCHING flag:

<ul>
<li><b>ContextSwitchCount</b></li>
<li><b>CycleTime</b></li>
<li><b>RetryCount</b></li>
<li><b>WaitReasonBitMap</b></li>
</ul>
The following members are set when you specify the READ_THREAD_PROFILING_FLAG_HARDWARE_COUNTERS flag:

<ul>
<li><b>HwCounters</b></li>
<li><b>HwCountersCount</b></li>
</ul>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-readthreadprofilingdata">ReadThreadProfilingData</a>