---
UID: NF:winbase.EnableThreadProfiling
title: EnableThreadProfiling function (winbase.h)
description: Enables thread profiling on the specified thread.
helpviewer_keywords: ["EnableThreadProfiling","EnableThreadProfiling function [Hardware Counter Profiling]","hcp.enablethreadprofiling","winbase/EnableThreadProfiling"]
old-location: hcp\enablethreadprofiling.htm
tech.root: hcp
ms.assetid: dbbe5b01-cabf-42cb-9ed9-c2c143f9923b
ms.date: 12/05/2018
ms.keywords: EnableThreadProfiling, EnableThreadProfiling function [Hardware Counter Profiling], hcp.enablethreadprofiling, winbase/EnableThreadProfiling
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnableThreadProfiling
 - winbase/EnableThreadProfiling
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - EnableThreadProfiling
---

# EnableThreadProfiling function


## -description

Enables thread profiling on the specified thread.

## -parameters

### -param ThreadHandle [in]

The handle to the thread on which you want to enable profiling. This must be the current thread.

### -param Flags [in]

To receive thread profiling data such as context switch count, set this parameter to THREAD_PROFILING_FLAG_DISPATCH; otherwise, set to 0.

### -param HardwareCounters [in]

To receive hardware performance counter data, set this parameter to a bitmask that identifies the hardware counters to collect. You can specify up to 16 performance counters. Each bit relates directly to the zero-based hardware counter index for the hardware performance counters that you configured. Set to zero if you are not collecting hardware counter data. If you set a bit for a hardware counter that has not been configured, the counter value that is read for that counter is zero.

### -param PerformanceDataHandle [out]

An opaque handle that you use when calling the <a href="/windows/desktop/api/winbase/nf-winbase-readthreadprofilingdata">ReadThreadProfilingData</a> and <a href="/windows/desktop/api/winbase/nf-winbase-disablethreadprofiling">DisableThreadProfiling</a> functions.

## -returns

 Returns ERROR_SUCCESS if the call is successful; otherwise, a system error code (see Winerror.h).

## -remarks

You must call the <a href="/windows/desktop/api/winbase/nf-winbase-disablethreadprofiling">DisableThreadProfiling</a> function before exiting the thread.

To profile hardware performance counters, you need a driver to configure the counters. The performance counters are configured globally for the system, so every thread has access to the same hardware counter data. The counters must be configured before you enable profiling. For information on configuring hardware performance counters, see the <b>KeSetHardwareCounterConfiguration</b> function in the Windows Driver Kit (WDK).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-disablethreadprofiling">DisableThreadProfiling</a>



<a href="/windows/desktop/api/winbase/nf-winbase-querythreadprofiling">QueryThreadProfiling</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readthreadprofilingdata">ReadThreadProfilingData</a>