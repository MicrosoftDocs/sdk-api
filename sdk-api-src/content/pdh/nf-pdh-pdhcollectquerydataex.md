---
UID: NF:pdh.PdhCollectQueryDataEx
title: PdhCollectQueryDataEx function (pdh.h)
description: Uses a separate thread to collect the current raw data value for all counters in the specified query. The function then signals the application-defined event and waits the specified time interval before returning.
helpviewer_keywords: ["PdhCollectQueryDataEx","PdhCollectQueryDataEx function [Perf]","_win32_pdhcollectquerydataex","base.pdhcollectquerydataex","pdh/PdhCollectQueryDataEx","perf.pdhcollectquerydataex"]
old-location: perf\pdhcollectquerydataex.htm
tech.root: perf
ms.assetid: 3fa1d193-03d0-44d8-a32b-b7754594d0ca
ms.date: 12/05/2018
ms.keywords: PdhCollectQueryDataEx, PdhCollectQueryDataEx function [Perf], _win32_pdhcollectquerydataex, base.pdhcollectquerydataex, pdh/PdhCollectQueryDataEx, perf.pdhcollectquerydataex
req.header: pdh.h
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
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PdhCollectQueryDataEx
 - pdh/PdhCollectQueryDataEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-eventing-pdh-l1-1-3.dll
 - Pdh.dll
api_name:
 - PdhCollectQueryDataEx
---

# PdhCollectQueryDataEx function


## -description

Uses a separate thread to collect the current raw data value for all counters in the specified query. The function then signals the application-defined event and waits the specified time interval before returning.

## -parameters

### -param hQuery [in]

Handle of the query. The query identifies the counters that you want to collect. The 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a> function returns this handle.

### -param dwIntervalTime [in]

Time interval to wait, in seconds.

### -param hNewDataEvent [in]

Handle to the event that you want PDH to signal after the time interval expires. To create an event object, call the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a> or a 
<a href="/windows/desktop/PerfCtrs/pdh-error-codes">PDH error code</a>. The following are possible values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The query handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
The query does not currently have any counters.

</td>
</tr>
</table>

## -remarks

PDH terminates the thread when you call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhclosequery">PdhCloseQuery</a> function. If you call <b>PdhCollectQueryDataEx</b> more than once, each subsequent call terminates the thread from the previous call and then starts a new thread.

When 
<b>PdhCollectQueryDataEx</b> is called for data from one counter instance only and the counter instance does not exist, the function returns PDH_NO_DATA. However, if data from more than one counter is queried, 
<b>PdhCollectQueryDataEx</b> may return ERROR_SUCCESS even if one of the counter instances does not yet exist. This is because it is not known if the specified counter instance does not exist, or if it will exist but has not yet been created. In this case, call 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a> or 
<a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a> for each of the counter instances of interest to determine whether they exist.

PDH stores the raw counter values for the current and previous collection. If you want to retrieve the current raw counter value, call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcountervalue">PdhGetRawCounterValue</a> function. If you want to compute a displayable value for the counter value, call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcountervalue">PdhGetFormattedCounterValue</a>. If the counter path contains a wildcard for the instance name, instead call the <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetrawcounterarraya">PdhGetRawCounterArray</a> and <a href="/windows/desktop/api/pdh/nf-pdh-pdhgetformattedcounterarraya">PdhGetFormattedCounterArray</a> functions, respectively.


#### Examples

The following example shows how to use this function.


```cpp

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <pdh.h>

#pragma comment(lib, "pdh.lib")

CONST PWSTR COUNTER_NAME    = L"\\Processor(0)\\% Processor Time";
CONST ULONG SAMPLE_COUNT    = 10;
CONST ULONG SAMPLE_INTERVAL = 2;

void wmain(void)
{
    PDH_STATUS Status;
    HANDLE Event = NULL;
    PDH_HQUERY Query = NULL;
    PDH_HCOUNTER Counter;
    ULONG WaitResult;
    ULONG CounterType;
    PDH_FMT_COUNTERVALUE DisplayValue;

    Status = PdhOpenQuery(NULL, 0, &Query);
    if (Status != ERROR_SUCCESS) 
    {
        wprintf(L"\nPdhOpenQuery failed with status 0x%x.", Status);
        goto Cleanup;
    }

    Status = PdhAddCounter(Query, COUNTER_NAME, 0, &Counter);
    if (Status != ERROR_SUCCESS) 
    {
        wprintf(L"\nPdhAddCounter failed with 0x%x.", Status);
        goto Cleanup;
    }

    //
    // Calculating the formatted value of some counters requires access to the
    // value of a previous sample. Make this call to get the first sample value
    // populated, to be used later for calculating the next sample.
    //

    Status = PdhCollectQueryData(Query);
    if (Status != ERROR_SUCCESS) 
    {
        wprintf(L"\nPdhCollectQueryData failed with status 0x%x.", Status);
        goto Cleanup;
    }

    //
    // This will create a separate thread that will collect raw counter data
    // every 2 seconds and set the supplied Event.
    //

    Event = CreateEvent(NULL, FALSE, FALSE, L"MyEvent");
    if (Event == NULL) 
    {
        wprintf(L"\nCreateEvent failed with status 0x%x.", GetLastError());
        goto Cleanup;
    }

    Status = PdhCollectQueryDataEx(Query, SAMPLE_INTERVAL, Event);
    if (Status != ERROR_SUCCESS) 
    {
        wprintf(L"\nPdhCollectQueryDataEx failed with status 0x%x.", Status);
        goto Cleanup;
    }

    //
    // Collect and format 10 samples, 2 seconds apart.
    //

    for (ULONG i = 0; i < SAMPLE_COUNT; i++) 
    {
        WaitResult = WaitForSingleObject(Event, INFINITE);

        if (WaitResult == WAIT_OBJECT_0) 
        {
            Status = PdhGetFormattedCounterValue(Counter, PDH_FMT_DOUBLE, &CounterType, &DisplayValue);

            if (Status == ERROR_SUCCESS) 
            {
                wprintf(L"\nCounter Value: %.20g", DisplayValue.doubleValue);
            } 
            else 
            {
                wprintf(L"\nPdhGetFormattedCounterValue failed with status 0x%x.", Status);
                goto Cleanup;
            }
        } 
        else if (WaitResult == WAIT_FAILED) 
        {
            wprintf(L"\nWaitForSingleObject failed with status 0x%x.", GetLastError());
            goto Cleanup;
        }
    }

Cleanup:

    if (Event) 
    {
        CloseHandle(Event);
    }

    //
    // This will close both the Query handle and all associated Counter handles
    // returned by PdhAddCounter.
    //

    if (Query) 
    {
        PdhCloseQuery(Query);
    }
}

```

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhcollectquerydata">PdhCollectQueryData</a>



<a href="/windows/desktop/api/pdh/nf-pdh-pdhopenquerya">PdhOpenQuery</a>