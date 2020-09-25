---
UID: NC:winperf.PM_COLLECT_PROC
title: PM_COLLECT_PROC (winperf.h)
description: Collects the performance data and returns it to the consumer.
helpviewer_keywords: ["CollectPerformanceData","CollectPerformanceData callback function [Perf]","PM_COLLECT_PROC","PM_COLLECT_PROC callback","base.collectperformancedata","perf.collectperformancedata","winperf/CollectPerformanceData"]
old-location: perf\collectperformancedata.htm
tech.root: perf
ms.assetid: 9903eb4b-017b-47df-81c5-98c4e1ac697d
ms.date: 24/09/2020
ms.keywords: CollectPerformanceData, CollectPerformanceData callback function [Perf], PM_COLLECT_PROC, PM_COLLECT_PROC callback, base.collectperformancedata, perf.collectperformancedata, winperf/CollectPerformanceData
req.header: winperf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PM_COLLECT_PROC
 - winperf/PM_COLLECT_PROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winperf.h
api_name:
 - CollectPerformanceData
---

# PM_COLLECT_PROC callback function

## -description

Collects the performance data and returns it to the consumer. Implement and export this function if you are writing a performance DLL to provide performance data. The system calls this function whenever a consumer queries the registry for performance data. 

The **CollectPerformanceData** function is a placeholder for the application-defined function name.

## -parameters

### -param lpValueName [in, optional]

Type: **LPWSTR**

Null-terminated string that contains the query string (for example, "Global" or "238") passed to the [RegQueryValueEx](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function. For the query string format, see [Using the Registry Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-registry-functions-to-consume-counter-data).

> [!NOTE]
> This parameter is annotated as optional (nullable). The semantics of a null query was never explained, however, in practice it never happens to be null. Furthermore, queries against performance counters **HKEY**s via **RegQueryValueEx** are meaningless without a valid *lpValueName* parameter, which is exactly this query string. Running such null query results in `Error Code 0x00000057: The parameter is incorrect.`
>
> With that being said, you should always verify input data, and if this parameter turns out to be null, the callback function should fail early. Check descriptions of other parameters on how to fail properly.

### -param lppData [in, out]

Type: **LPVOID \***

Consumer-allocated buffer that will contain the performance data.

Here, *pData* refers to the pointer pointed by *lppData*, i.e. `*lppData = pData`.

On output, set *pData* to one byte past the end of your data. The data must conform to the 
[PERF_OBJECT_TYPE](ns-winperf-perf_object_type.md) structure.

If this function fails, leave the *pData* pointer value unchanged.

### -param lpcbTotalBytes [in, out]

Type: **LPDWORD**

On input, specifies the size, in bytes, of the *pData* buffer.

On output, set *lpcbTotalBytes* to the size, in bytes, of the data written to the *pData* buffer. The size must be 8-byte aligned.

If this function fails, set *lpcbTotalBytes* to zero.

### -param lpNumObjectTypes [in, out]

Type: **LPDWORD**

Set *lpNumObjectTypes* to the number of object [types](ns-winperf-perf_object_type.md) (not [instances](ns-winperf-perf_instance_definition.md)) written to the *pData* buffer.

If this function fails, set *lpNumObjectTypes* to zero.

> [!NOTE]
> This parameter is annotated as both *In* and *Out*. Actually the pointee (the value behind this pointer) is never used as an input, and there are no contracts about its content upon function callback invokation: it is best to assume that the pointee is uninitialized and contains garbage data.

## -returns

Return one of the following return values only.

| Return code | Description |
|-------------|-------------|
| **ERROR_MORE_DATA** | The size of the *pData* buffer as specified by *lpcbTotalBytes* is not large enough to store the data. Leave *pData* unchanged, and set *lpcbTotalBytes* and *lpNumObjectTypes* to zero. No attempt is made to indicate the required buffer size, because this can change before the next call. |
| **ERROR_SUCCESS** | Return this value in all cases other than the **ERROR_MORE_DATA** case, even if no data is returned or an error occurs. To report errors other than insufficient buffer size, use the Application Event Log. |

## -remarks

If the requested objects specified in the *lpValueName* parameter do not correspond to any of the object indexes that your performance DLL supports, leave the *pData* parameter unchanged, and set the *lpcbTotalBytes* and *lpNumObjectTypes* parameters to zero. This indicates that no data was returned.

If you support one or more of the queried objects, determine whether the size of the *pData* buffer as specified by *lpcbTotalBytes* is large enough to store the data. If not, leave *pData* unchanged, and set *lpcbTotalBytes* and *lpNumObjectTypes* to zero. No attempt is made to indicate the required buffer size, because this may change before the next call. Return **ERROR_MORE_DATA**.

If your data collection is time-consuming, you should respond only to queries for specific objects and `Costly` queries. You should also lower the priority of the thread collecting the data, so that it does not adversely affect system performance. For the query string format, see [Using the Registry Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-registry-functions-to-consume-counter-data).

If the consumer is running on another computer (remotely), then the <a href="/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)">OpenPerformanceData</a>, [ClosePerformanceData](/windows/desktop/api/winperf/nc-winperf-pm_close_proc), and **CollectPerformanceData** functions are called in the context of the Winlogon process, which handles the server side of the remote connection. This distinction is important when troubleshooting problems that occur only remotely.

After your function returns successfully, the system can perform some basic tests to ensure the integrity of the data. By default, no tests are performed. If a test fails, the system generates an event log message and the data is discarded to prevent any further problems due to pointers that are not valid. The following registry value controls the test level: `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib\ExtCounterTestLevel`.

The following are the possible test levels for **ExtCounterTestLevel**. 

| Level | Meaning |
|-------|---------|
| 1 | Test the pointers and buffers of trusted counter DLLs. Sends a copy of the user's buffer. |
| 2 | Test pointers and buffer lengths but does not test pointer references or buffer contents. Sends a copy of the user's buffer. |
| 3 | Do not test pointers or buffers. Sends a copy of the user's buffer. |
| 4 | Do not test pointers or buffers. Sends the user's buffer, not a copy. This is the default value. |

The following tests are performed at levels 1 and 2:

- Verifies that the value of *lpcbTotalBytes* is consistent with the returned buffer pointer, *pData*. If you add the *lpcbTotalBytes* value to the original buffer pointer passed to this function, you should end up with the same buffer pointer returned by this function. If they are not the same, a error message is logged and the data is ignored.
- Verify that a buffer overrun did not occur. The system adds a 1-KB guard page before and after the consumer-allocated buffer. If the returned buffer pointer, *pData*, points past the first byte of the appended guard page, then it is assumed that the buffer is not valid and the data is ignored. If the buffer pointer exceeds the end of the buffer, but not the end of the guard page, then a buffer overrun error is logged. If the buffer pointer is past the end of the guard page, then a heap error is logged because the heap that the buffer was allocated from could have been corrupted, causing other memory errors.
- Verify that the guard pages have not been corrupted. The 1-KB guard pages that were added before and after the buffer are initialized with a data pattern before this function is called. This data pattern is checked after the collect procedure returns. If any discrepancy is detected, a buffer overrun or other memory error is assumed and the data is ignored.

The following tests are performed only if test level 1 is used:

- Verify that the sum of each object's **TotalByteLength** member is the same as the value of *lpcbTotalBytes*. If not, the data is ignored.
- Verify that the **ByteLength** member of each instance is consistent. The lengths are consistent if the next object or end of buffer follows the last instance. If not, the data is ignored.

#### Examples

For an example, see [Implementing CollectPerformanceData](/windows/desktop/PerfCtrs/implementing-collectperformancedata).

## -see-also

- <a href="/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)">OpenPerformanceData</a>
- [ClosePerformanceData](/windows/desktop/api/winperf/nc-winperf-pm_close_proc)
