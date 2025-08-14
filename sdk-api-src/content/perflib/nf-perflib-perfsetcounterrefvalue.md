---
UID: NF:perflib.PerfSetCounterRefValue
title: PerfSetCounterRefValue function (perflib.h)
description: Updates the value of a counter whose value is a pointer to the actual data. Providers use this function.
helpviewer_keywords: ["PerfSetCounterRefValue","PerfSetCounterRefValue function [Perf]","base.perfsetcounterrefvalue","perf.perfsetcounterrefvalue","perflib/PerfSetCounterRefValue"]
old-location: perf\perfsetcounterrefvalue.htm
tech.root: perf
ms.assetid: 0694ff8c-4c36-4bf7-a2b3-c032bf7a2f65
ms.date: 12/05/2018
ms.keywords: PerfSetCounterRefValue, PerfSetCounterRefValue function [Perf], base.perfsetcounterrefvalue, perf.perfsetcounterrefvalue, perflib/PerfSetCounterRefValue
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
 - PerfSetCounterRefValue
 - perflib/PerfSetCounterRefValue
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
 - PerfSetCounterRefValue
---

# PerfSetCounterRefValue function


## -description

Updates the value of a counter whose value is a pointer to the actual data. Providers use this function.

## -parameters

### -param Provider [in]

The handle of the provider. Use the handle variable that the <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element.

<b>Windows Vista:  </b>The <a href="/windows/desktop/api/perflib/nf-perflib-perfstartprovider">PerfStartProvider</a> function returns the handle.

### -param Instance [in]

A <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> structure that contains the counter set instance. The <a href="/windows/desktop/api/perflib/nf-perflib-perfcreateinstance">PerfCreateInstance</a> function returns this pointer.

### -param CounterId [in]

Identifier that uniquely identifies the counter to update in the instance block. The identifier is defined in the <b>id</b> attribute of the <a href="/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element">counter</a> element and must match the <b>CounterId</b> member of one of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_info">PERF_COUNTER_INFO</a> structures in the instance block. Use the counter ID constant that the <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the constant, see the <b>symbol</b> attribute of the <b>counter</b> element.

<b>Windows Vista:  </b>The counter ID constant is not available.

### -param Address [in]

Pointer to the actual counter data. 

If <b>NULL</b>, the consumer receives ERROR_NO_DATA.

To indicate that the counter data is accessed by reference, the counter declaration in the manifest must include a <a href="/previous-versions/aa371909(v=vs.85)">counterAttribute</a> element whose <b>name</b> attribute is set to "reference".

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

This is a convenience function for specifying a reference to the raw counter data. To update the reference to the raw counter data yourself, use the <b>Offset</b> member of the <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_info">PERF_COUNTER_INFO</a> structure to access the counter value for a specific counter. The <b>Attrib</b> member must include the PERF_ATTRIB_BY_REFERENCE flag. The <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> structure block contains one or more counter information structures.

Depending on the counter type, the pointer must reference a 4-byte or 8-byte unsigned integer. When collecting the counter data, PERFLIB dereferences the pointer and returns the actual data.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfsetulongcountervalue">PerfSetULongCounterValue</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfsetulonglongcountervalue">PerfSetULongLongCounterValue</a>