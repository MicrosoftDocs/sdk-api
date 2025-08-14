---
UID: NF:perflib.PerfQueryInstance
title: PerfQueryInstance function (perflib.h)
description: Retrieves a pointer to the specified counter set instance. Providers use this function.
helpviewer_keywords: ["PerfQueryInstance","PerfQueryInstance function [Perf]","base.perfqueryinstance","perf.perfqueryinstance","perflib/PerfQueryInstance"]
old-location: perf\perfqueryinstance.htm
tech.root: perf
ms.assetid: 844f3f9e-8de2-4995-b13c-befe0da8a1ab
ms.date: 12/05/2018
ms.keywords: PerfQueryInstance, PerfQueryInstance function [Perf], base.perfqueryinstance, perf.perfqueryinstance, perflib/PerfQueryInstance
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
 - PerfQueryInstance
 - perflib/PerfQueryInstance
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
 - PerfQueryInstance
---

# PerfQueryInstance function


## -description

Retrieves a pointer to the specified counter set instance. Providers use this function.

## -parameters

### -param ProviderHandle [in]

The handle of the provider. Use the handle variable that the <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element.

<b>Windows Vista:  </b>The <a href="/windows/desktop/api/perflib/nf-perflib-perfstartprovider">PerfStartProvider</a> function returns the handle.

### -param CounterSetGuid [in]

GUID that uniquely identifies the counter set that you want to query. This is the same GUID specified in the <b>guid</b> attribute of the <a href="/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element">counterSet</a> element. Use the GUID variable that the <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <b>counterSet</b> element.

<b>Windows Vista:  </b>The GUID variable is not available.

### -param Name [in]

<b>Null</b>-terminated Unicode string that contains the name of counter set instance that you want to retrieve.

### -param Id [in]

Unique identifier of the counter set instance that you want to retrieve.

## -returns

A <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_instance">PERF_COUNTERSET_INSTANCE</a> structure that contains the counter set instance or <b>NULL</b> if the instance does not exist.

This function returns <b>NULL</b> if an error occurred. To determine the error that occurred, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Use the same instance name and identifier that you used when calling <a href="/windows/desktop/api/perflib/nf-perflib-perfcreateinstance">PerfCreateInstance</a> to retrieve a specific instance of the counter set.

Providers should  cache the pointer to the instance when they create the instance instead of calling this function to retrieve the pointer.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfcreateinstance">PerfCreateInstance</a>