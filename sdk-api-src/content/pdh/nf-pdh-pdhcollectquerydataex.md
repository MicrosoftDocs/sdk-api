---
UID: NF:pdh.PdhCollectQueryDataEx
title: PdhCollectQueryDataEx function
author: windows-driver-content
description: Uses a separate thread to collect the current raw data value for all counters in the specified query. The function then signals the application-defined event and waits the specified time interval before returning.
old-location: perf\pdhcollectquerydataex.htm
old-project: PerfCtrs
ms.assetid: 3fa1d193-03d0-44d8-a32b-b7754594d0ca
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: PdhCollectQueryDataEx, PdhCollectQueryDataEx function [Perf], _win32_pdhcollectquerydataex, base.pdhcollectquerydataex, pdh/PdhCollectQueryDataEx, perf.pdhcollectquerydataex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Pdh.dll
api_name:
-	PdhCollectQueryDataEx
product: Windows
targetos: Windows
req.lib: Pdh.lib
req.dll: Pdh.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PdhCollectQueryDataEx function


## -description


Uses a separate thread to collect the current raw data value for all counters in the specified query. The function then signals the application-defined event and waits the specified time interval before returning.
		


## -parameters




### -param hQuery [in]

Handle of the query. The query identifies the counters that you want to collect. The 
<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a> function returns this handle.


### -param dwIntervalTime [in]

Time interval to wait, in seconds. 


### -param hNewDataEvent [in]

Handle to the event that you want PDH to signal after the time interval expires. To create an event object, call the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function. 



					


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following are possible values.

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



PDH terminates the thread when you call the <a href="https://msdn.microsoft.com/af0fb9f4-3999-48fa-88d7-aa59b5caed75">PdhCloseQuery</a> function. If you call <b>PdhCollectQueryDataEx</b> more than once, each subsequent call terminates the thread from the previous call and then starts a new thread.

When 
<b>PdhCollectQueryDataEx</b> is called for data from one counter instance only and the counter instance does not exist, the function returns PDH_NO_DATA. However, if data from more than one counter is queried, 
<b>PdhCollectQueryDataEx</b> may return ERROR_SUCCESS even if one of the counter instances does not yet exist. This is because it is not known if the specified counter instance does not exist, or if it will exist but has not yet been created. In this case, call 
<a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a> or 
<a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a> for each of the counter instances of interest to determine whether they exist.

PDH stores the raw counter values for the current and previous collection. If you want to retrieve the current raw counter value, call the <a href="https://msdn.microsoft.com/bb246c82-8748-4e2f-9f44-a206199aff90">PdhGetRawCounterValue</a> function. If you want to compute a displayable value for the counter value, call the <a href="https://msdn.microsoft.com/cd104b26-1498-4f95-a411-97d868b43836">PdhGetFormattedCounterValue</a>. If the counter path contains a wildcard for the instance name, instead call the <a href="https://msdn.microsoft.com/03b30d08-6901-45cd-bd6d-d2672eb0f914">PdhGetRawCounterArray</a> and <a href="https://msdn.microsoft.com/0f388c7e-d0c8-461d-908c-48af92166996">PdhGetFormattedCounterArray</a> functions, respectively.


#### Examples

The following example shows how to use this function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
#include &lt;pdh.h&gt;

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

    Status = PdhOpenQuery(NULL, 0, &amp;Query);
    if (Status != ERROR_SUCCESS) 
    {
        wprintf(L"\nPdhOpenQuery failed with status 0x%x.", Status);
        goto Cleanup;
    }

    Status = PdhAddCounter(Query, COUNTER_NAME, 0, &amp;Counter);
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

    for (ULONG i = 0; i &lt; SAMPLE_COUNT; i++) 
    {
        WaitResult = WaitForSingleObject(Event, INFINITE);

        if (WaitResult == WAIT_OBJECT_0) 
        {
            Status = PdhGetFormattedCounterValue(Counter, PDH_FMT_DOUBLE, &amp;CounterType, &amp;DisplayValue);

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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/1d83325b-8deb-4731-9df4-6201da292cdc">PdhCollectQueryData</a>



<a href="https://msdn.microsoft.com/ec4e5353-c7f5-4957-b7f4-39df508846a0">PdhOpenQuery</a>
 

 

