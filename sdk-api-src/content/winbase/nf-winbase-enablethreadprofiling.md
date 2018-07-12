---
UID: NF:winbase.EnableThreadProfiling
title: EnableThreadProfiling function
author: windows-sdk-content
description: Enables thread profiling on the specified thread.
old-location: hcp\enablethreadprofiling.htm
old-project: hcp
ms.assetid: dbbe5b01-cabf-42cb-9ed9-c2c143f9923b
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: EnableThreadProfiling, EnableThreadProfiling function [Hardware Counter Profiling], hcp.enablethreadprofiling, winbase/EnableThreadProfiling
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - EnableThreadProfiling
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
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

An opaque handle that you use when calling the <a href="https://msdn.microsoft.com/e7335caf-d89b-45b4-831d-9ead4448a6a3">ReadThreadProfilingData</a> and <a href="https://msdn.microsoft.com/650631a6-fd90-46e1-8f2d-84aaaed05bac">DisableThreadProfiling</a> functions.


## -returns



 Returns ERROR_SUCCESS if the call is successful; otherwise, a system error code (see Winerror.h).




## -remarks



You must call the <a href="https://msdn.microsoft.com/650631a6-fd90-46e1-8f2d-84aaaed05bac">DisableThreadProfiling</a> function before exiting the thread.

To profile hardware performance counters, you need a driver to configure the counters. The performance counters are configured globally for the system, so every thread has access to the same hardware counter data. The counters must be configured before you enable profiling. For information on configuring hardware performance counters, see the <b>KeSetHardwareCounterConfiguration</b> function in the Windows Driver Kit (WDK).




## -see-also




<a href="https://msdn.microsoft.com/650631a6-fd90-46e1-8f2d-84aaaed05bac">DisableThreadProfiling</a>



<a href="https://msdn.microsoft.com/cf746694-cc3a-4791-8877-fd879e968811">QueryThreadProfiling</a>



<a href="https://msdn.microsoft.com/e7335caf-d89b-45b4-831d-9ead4448a6a3">ReadThreadProfilingData</a>
 

 

