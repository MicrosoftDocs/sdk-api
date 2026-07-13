---
UID: NF:perflib.PerfStartProvider
title: PerfStartProvider function (perflib.h)
description: Registers the provider. (PerfStartProvider)
helpviewer_keywords: ["PerfStartProvider","PerfStartProvider function [Perf]","base.perfstartprovider","perf.perfstartprovider","perflib/PerfStartProvider"]
old-location: perf\perfstartprovider.htm
tech.root: perf
ms.assetid: b417b19b-adbc-40e3-aca1-c2cd94a79232
ms.date: 12/05/2018
ms.keywords: PerfStartProvider, PerfStartProvider function [Perf], base.perfstartprovider, perf.perfstartprovider, perflib/PerfStartProvider
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
 - PerfStartProvider
 - perflib/PerfStartProvider
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
 - PerfStartProvider
---

# PerfStartProvider function


## -description

Registers the provider.

## -parameters

### -param ProviderGuid [in]

GUID that uniquely identifies the provider. The <b>providerGuid</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element specifies the GUID.

### -param ControlCallback [in, optional]

<a href="/windows/desktop/api/perflib/nc-perflib-perflibrequest">ControlCallback</a> function that PERFLIB calls to notify you of consumer requests, such as a request to add or remove counters from the query. This parameter is set if the <b>callback</b> attribute of the <b>counters</b> element is "custom"; otherwise, <b>NULL</b>.

### -param phProvider [out]

Handle to the provider. You must call <a href="/windows/desktop/api/perflib/nf-perflib-perfstopprovider">PerfStopProvider</a> to release resources associated with the handle.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The <a href="/windows/desktop/PerfCtrs/counterinitialize">CounterInitialize</a> function calls this function; do not call this function directly.

<b>Windows Vista:  </b>The <b>PerfAutoInitialize</b> function calls this function.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfstopprovider">PerfStopProvider</a>
