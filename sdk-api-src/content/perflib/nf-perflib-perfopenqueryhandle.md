---
UID: NF:perflib.PerfOpenQueryHandle
title: PerfOpenQueryHandle function (perflib.h)
description: Creates a handle that references a query on the specified system. A query is a list of counter specifications.
helpviewer_keywords: ["PerfOpenQueryHandle","PerfOpenQueryHandle function [Perf]","perf.perfopenqueryhandle","perflib/PerfOpenQueryHandle"]
old-location: perf\perfopenqueryhandle.htm
tech.root: perf
ms.assetid: 5105F617-9443-451D-B802-C6A241769E65
ms.date: 12/05/2018
ms.keywords: PerfOpenQueryHandle, PerfOpenQueryHandle function [Perf], perf.perfopenqueryhandle, perflib/PerfOpenQueryHandle
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: AdvAPI32.lib
req.dll: AdvAPI32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PerfOpenQueryHandle
 - perflib/PerfOpenQueryHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-perf-legacy-l1-1-0.dll
 - AdvAPI32.dll
api_name:
 - PerfOpenQueryHandle
---

# PerfOpenQueryHandle function


## -description

Creates a handle that references a query on the specified system. A query is a
list of counter specifications.

## -parameters

### -param szMachine [in, optional]

The name of the machine for which you want to get the query handle.

### -param phQuery [out]

The handle to the query. Call <a href="/windows/desktop/api/perflib/nf-perflib-perfclosequeryhandle">PerfCloseQueryHandle</a> to close ths handle when you no longer need it.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

Use <a href="/windows/desktop/api/perflib/nf-perflib-perfaddcounters">PerfAddCounters</a> and <a href="/windows/desktop/api/perflib/nf-perflib-perfdeletecounters">PerfDeleteCounters</a> to
add or remove counter specifications to the list. Use <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterinfo">PerfQueryCounterInfo</a> to
get the counter specifications currently in the list and to determine the
indexes at which the data for each counter will be returned by 
<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a>. Use <b>PerfQueryCounterData</b> to retrieve the values of the
counters that match the counter specifications.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfaddcounters">PerfAddCounters</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfclosequeryhandle">PerfCloseQueryHandle</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfdeletecounters">PerfDeleteCounters</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterinfo">PerfQueryCounterInfo</a>