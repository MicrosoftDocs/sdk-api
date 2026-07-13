---
UID: NF:perflib.PerfCloseQueryHandle
title: PerfCloseQueryHandle function (perflib.h)
description: Closes a query handle that you opened by calling PerfOpenQueryHandle.
helpviewer_keywords: ["PerfCloseQueryHandle","PerfCloseQueryHandle function [Perf]","perf.perfclosequeryhandle","perflib/PerfCloseQueryHandle"]
old-location: perf\perfclosequeryhandle.htm
tech.root: perf
ms.assetid: 94D08CF1-D47C-4A1B-A0CE-8C318CDF9FE0
ms.date: 12/05/2018
ms.keywords: PerfCloseQueryHandle, PerfCloseQueryHandle function [Perf], perf.perfclosequeryhandle, perflib/PerfCloseQueryHandle
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
 - PerfCloseQueryHandle
 - perflib/PerfCloseQueryHandle
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
 - PerfCloseQueryHandle
---

# PerfCloseQueryHandle function


## -description

Closes a query handle that you opened by calling <a href="/windows/desktop/api/perflib/nf-perflib-perfopenqueryhandle">PerfOpenQueryHandle</a>.

## -parameters

### -param hQuery [in]

A handle to the query that you want to close

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfopenqueryhandle">PerfOpenQueryHandle</a>