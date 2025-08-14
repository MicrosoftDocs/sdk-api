---
UID: NF:perflib.PerfSetCounterSetInfo
title: PerfSetCounterSetInfo function (perflib.h)
description: Specifies the layout of a particular counter set.
helpviewer_keywords: ["PerfSetCounterSetInfo","PerfSetCounterSetInfo function [Perf]","base.perfsetcountersetinfo","perf.perfsetcountersetinfo","perflib/PerfSetCounterSetInfo"]
old-location: perf\perfsetcountersetinfo.htm
tech.root: perf
ms.assetid: b4295503-5588-4898-816c-939a5920fc77
ms.date: 12/05/2018
ms.keywords: PerfSetCounterSetInfo, PerfSetCounterSetInfo function [Perf], base.perfsetcountersetinfo, perf.perfsetcountersetinfo, perflib/PerfSetCounterSetInfo
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
 - PerfSetCounterSetInfo
 - perflib/PerfSetCounterSetInfo
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
 - PerfSetCounterSetInfo
---

# PerfSetCounterSetInfo function


## -description

Specifies the layout of a particular counter set.

## -parameters

### -param ProviderHandle [in]

The handle of the provider. Use the handle variable that the <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool generated for you. For the name of the variable, see the <b>symbol</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element.

<b>Windows Vista:  </b>The <a href="/windows/desktop/api/perflib/nf-perflib-perfstartprovider">PerfStartProvider</a> function returns the handle.

### -param Template [in]

Buffer that contains the counter set information. For details, see <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_info">PERF_COUNTERSET_INFO</a>.

### -param TemplateSize [in]

Size, in bytes, of the <i>pTemplate</i> buffer.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The <a href="/windows/desktop/PerfCtrs/counterinitialize">CounterInitialize</a> function calls this function; do not call this function directly.

<b>Windows Vista:  </b>The <b>PerfAutoInitialize</b> function calls this function.