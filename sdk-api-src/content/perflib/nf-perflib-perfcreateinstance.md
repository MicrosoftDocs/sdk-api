---
UID: NF:perflib.PerfCreateInstance
title: PerfCreateInstance function (perflib.h)
description: Creates an instance of the specified counter set.
helpviewer_keywords: ["PerfCreateInstance","PerfCreateInstance function [Perf]","base.perfcreateinstance","perf.perfcreateinstance","perflib/PerfCreateInstance"]
old-location: perf\perfcreateinstance.htm
tech.root: perf
ms.assetid: 73be8588-2c87-4c27-933d-62b8605ed9a3
ms.date: 12/05/2018
ms.keywords: PerfCreateInstance, PerfCreateInstance function [Perf], base.perfcreateinstance, perf.perfcreateinstance, perflib/PerfCreateInstance
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
 - PerfCreateInstance
 - perflib/PerfCreateInstance
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
 - PerfCreateInstance
---

# PerfCreateInstance function


## -description

Creates an instance of the specified counter set. Providers use this function.

## -parameters

### -param ProviderHandle [in]

The handle of the provider. Use the handle variable that the <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element.

<b>Windows Vista:  </b>The <a href="/windows/desktop/api/perflib/nf-perflib-perfstartprovider">PerfStartProvider</a> function returns the handle.

### -param CounterSetGuid [in]

GUID that uniquely identifies the counter set that you want to create an instance of. This is the same GUID specified in the <b>guid</b> attribute of the <a href="/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element">counterSet</a> element. Use the GUID variable that the <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <b>counterSet</b> element.

<b>Windows Vista:  </b>The GUID variable is not available.

### -param Name [in]

<b>Null</b>-terminated Unicode string that contains a unique name for this instance.

### -param Id [in]

Unique identifier for this instance of the counter set. The identifier can be a serial number that you increment for each new instance.

## -returns

A <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> structure that contains the instance of the counter set or <b>NULL</b> if PERFLIB could not create the instance. Cache this pointer to use in later calls instead of calling <a href="/windows/desktop/api/perflib/nf-perflib-perfqueryinstance">PerfQueryInstance</a> to retrieve the pointer to the instance.

This function returns <b>NULL</b> if an error occurred. To determine the error that occurred, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The provider determines when it creates an instance. If the counter data is more static, the provider can create an instance at initialization time. For example, the number of processors on a computer would be considered static, so a provider that provides counter data for processors could create an instance for each processor on the computer at initialization time. For counters that are more dynamic, such as disk or process counters, the providers would create the new instances in response to a new USB device being added or a new process being created.

When the provider calls this function, PERFLIB allocates local memory for the new instance and builds the instance block. PERFLIB deletes the memory when the provider calls the <a href="/windows/desktop/api/perflib/nf-perflib-perfdeleteinstance">PerfDeleteInstance</a> function.

The instance contains the raw counter data. Providers use the following three functions to update the raw counter data:

<ul>
<li>
<a href="/windows/desktop/api/perflib/nf-perflib-perfsetulongcountervalue">PerfSetUlongCounterValue</a>
</li>
<li>
<a href="/windows/desktop/api/perflib/nf-perflib-perfsetulonglongcountervalue">PerfSetUlongLongCounterValue</a>
</li>
<li>
<a href="/windows/desktop/api/perflib/nf-perflib-perfsetcounterrefvalue">PerfSetCounterRefValue</a>
</li>
</ul>
Typically, the provider keeps the counter data up-to-date at all times. As an alternative, the provider can implement the <a href="/windows/desktop/api/perflib/nc-perflib-perflibrequest">ControlCallback</a> function and use the <b>PERF_COLLECT_START</b> request code to trigger the updates.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfdeleteinstance">PerfDeleteInstance</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfqueryinstance">PerfQueryInstance</a>