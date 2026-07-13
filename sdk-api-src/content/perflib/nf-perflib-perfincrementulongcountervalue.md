---
UID: NF:perflib.PerfIncrementULongCounterValue
title: PerfIncrementULongCounterValue function (perflib.h)
description: Increments the value of a counter whose value is a 4-byte unsigned integer. Providers use this function.
helpviewer_keywords: ["PerfIncrementULongCounterValue","PerfIncrementULongCounterValue function [Perf]","perf.perfincrementulongcountervalue","perflib/PerfIncrementULongCounterValue"]
old-location: perf\perfincrementulongcountervalue.htm
tech.root: perf
ms.assetid: 002162a0-d782-4648-949e-178985fd1d44
ms.date: 12/05/2018
ms.keywords: PerfIncrementULongCounterValue, PerfIncrementULongCounterValue function [Perf], perf.perfincrementulongcountervalue, perflib/PerfIncrementULongCounterValue
req.header: perflib.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PerfIncrementULongCounterValue
 - perflib/PerfIncrementULongCounterValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-perfcounters-l1-2-0.dll
 - Advapi32.dll
 - API-MS-Win-Core-perfcounters-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PerfIncrementULongCounterValue
---

# PerfIncrementULongCounterValue function


## -description

Increments the value of a counter whose value is a 4-byte unsigned integer.  Providers use this function.

## -parameters

### -param Provider [in]

The handle of the provider. Use the handle variable that the <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element.

<b>Windows Vista:  </b>The <a href="/windows/desktop/api/perflib/nf-perflib-perfstartprovider">PerfStartProvider</a> function returns the handle.

### -param Instance [in]

A <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> structure that contains the counter set instance. The <a href="/windows/desktop/api/perflib/nf-perflib-perfcreateinstance">PerfCreateInstance</a> function returns this pointer.

### -param CounterId [in]

Identifier that uniquely identifies the counter to update in the instance block. The identifier is defined in the <b>id</b> attribute of the <a href="/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element">counter</a> element and must match the <b>CounterId</b> member of one of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_info">PERF_COUNTER_INFO</a> structures in the instance block. Use the counter ID constant that the <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the constant, see the <b>symbol</b> attribute of the <b>counter</b> element.

<b>Windows Vista:  </b>The counter ID constant is not available.

### -param Value [in]

Value by which to increment the counter.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

This is a convenience function for incrementing raw counter data. To increment the raw counter data yourself, use the <b>Offset</b> member of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_info">PERF_COUNTER_INFO</a> structure to access the raw counter data for a specific counter. The <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> structure block contains one or more counter information structures.

Use the <a href="/windows/desktop/api/perflib/nf-perflib-perfsetulongcountervalue">PerfSetULongCounterValue</a> function to initially set the counter value.

Note that the counter value will overflow when the counter value increments past the maximum size of a 4-byte unsigned integer.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfdecrementulongcountervalue">PerfDecrementULongCounterValue</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfincrementulonglongcountervalue">PerfIncrementULongLongCounterValue</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfsetulongcountervalue">PerfSetULongCounterValue</a>