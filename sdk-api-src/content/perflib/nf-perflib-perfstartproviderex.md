---
UID: NF:perflib.PerfStartProviderEx
title: PerfStartProviderEx function (perflib.h)
description: Registers the provider. (PerfStartProviderEx)
helpviewer_keywords: ["PerfStartProviderEx","PerfStartProviderEx function [Perf]","perf.perfstartproviderex","perflib/PerfStartProviderEx"]
old-location: perf\perfstartproviderex.htm
tech.root: perf
ms.assetid: 9f3aefbf-0836-46fc-8a53-858c3c94cef9
ms.date: 12/05/2018
ms.keywords: PerfStartProviderEx, PerfStartProviderEx function [Perf], perf.perfstartproviderex, perflib/PerfStartProviderEx
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
 - PerfStartProviderEx
 - perflib/PerfStartProviderEx
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
 - PerfStartProviderEx
---

# PerfStartProviderEx function


## -description

Registers the provider.

## -parameters

### -param ProviderGuid [in]

GUID that uniquely identifies the provider. The <b>providerGuid</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element specifies the GUID.

### -param ProviderContext [in, optional]

A <a href="/windows/win32/api/perflib/ns-perflib-perf_provider_context">PERF_PROVIDER_CONTEXT</a> structure that contains pointers to the control callback, memory management routines, and context information.

### -param Provider [out]

Handle to the provider. You must call <a href="/windows/desktop/api/perflib/nf-perflib-perfstopprovider">PerfStopProvider</a> to release resources associated with the handle.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The <a href="/windows/desktop/PerfCtrs/counterinitialize">CounterInitialize</a> function calls this function; do not call this function directly.

<b>Windows Vista:  </b>The <b>PerfAutoInitialize</b> function calls this function.

The CTRPP tool includes this function instead of <a href="/windows/desktop/api/perflib/nf-perflib-perfstartprovider">PerfStartProvider</a> if you use the <b>-MemoryRoutines</b> argument or <b>-NotificationCallback</b> argument when calling <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a>, or if the <b>callback</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element is set to "custom".

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfstopprovider">PerfStopProvider</a>
