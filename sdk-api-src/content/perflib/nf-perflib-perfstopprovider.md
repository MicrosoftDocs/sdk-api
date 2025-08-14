---
UID: NF:perflib.PerfStopProvider
title: PerfStopProvider function (perflib.h)
description: Removes the provider's registration from the list of registered providers and frees all resources associated with the provider.
helpviewer_keywords: ["PerfStopProvider","PerfStopProvider function [Perf]","base.perfstopprovider","perf.perfstopprovider","perflib/PerfStopProvider"]
old-location: perf\perfstopprovider.htm
tech.root: perf
ms.assetid: 4b31f88b-cadc-4bee-bdea-9079cc14c140
ms.date: 12/05/2018
ms.keywords: PerfStopProvider, PerfStopProvider function [Perf], base.perfstopprovider, perf.perfstopprovider, perflib/PerfStopProvider
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
 - PerfStopProvider
 - perflib/PerfStopProvider
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
 - PerfStopProvider
---

# PerfStopProvider function


## -description

Removes the provider's registration from the list of registered providers and frees all resources associated with the provider.

## -parameters

### -param ProviderHandle [in]

Handle to the provider.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The <a href="/windows/desktop/PerfCtrs/countercleanup">CounterCleanup</a> function calls this function; do not call this function directly.

<b>Windows Vista:  </b>The <b>PerfAutoCleanup</b> function calls this function.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfstartprovider">PerfStartProvider</a>