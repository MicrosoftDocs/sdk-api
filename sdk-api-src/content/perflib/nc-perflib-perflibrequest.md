---
UID: NC:perflib.PERFLIBREQUEST
title: PERFLIBREQUEST (perflib.h)
description: Providers can implement this function to receive notification when consumers perform certain actions, such as adding or removing counters from a query.
helpviewer_keywords: ["ControlCallback","ControlCallback callback function [Perf]","PERFLIBREQUEST","PERFLIBREQUEST callback","PERF_ADD_COUNTER","PERF_COLLECT_END","PERF_COLLECT_START","PERF_ENUM_INSTANCES","PERF_REMOVE_COUNTER","base.controlcallback_perflibv2","perf.controlcallback_perflibv2","perflib/ControlCallback"]
old-location: perf\controlcallback_perflibv2.htm
tech.root: perf
ms.assetid: 0f771ab7-af42-481b-b2da-20dcdf49b82b
ms.date: 12/05/2018
ms.keywords: ControlCallback, ControlCallback callback function [Perf], PERFLIBREQUEST, PERFLIBREQUEST callback, PERF_ADD_COUNTER, PERF_COLLECT_END, PERF_COLLECT_START, PERF_ENUM_INSTANCES, PERF_REMOVE_COUNTER, base.controlcallback_perflibv2, perf.controlcallback_perflibv2, perflib/ControlCallback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PERFLIBREQUEST
 - perflib/PERFLIBREQUEST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Perflib.h
api_name:
 - ControlCallback
---

# PERFLIBREQUEST callback function


## -description

Providers can implement this function to receive notification when consumers perform certain actions, such as adding or removing counters from a query. 
			PERFLIB calls the callback before the consumer's request completes.

The <b>PERFLIBREQUEST</b> type defines a pointer to this callback function. The <b>ControlCallback</b> function is a placeholder for the application-defined function name.

## -parameters

### -param RequestCode [in]

The request code can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERF_ADD_COUNTER"></a><a id="perf_add_counter"></a><dl>
<dt><b>PERF_ADD_COUNTER</b></dt>
</dl>
</td>
<td width="60%">
The consumer is adding a counter to the query. PERFLIB calls the callback with this request code for each counter  being added to the query. The  <i>Buffer</i> parameter contains a <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identity">PERF_COUNTER_IDENTITY</a> structure that identifies the counter being added.

Providers can use this notification to start counting.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_REMOVE_COUNTER"></a><a id="perf_remove_counter"></a><dl>
<dt><b>PERF_REMOVE_COUNTER</b></dt>
</dl>
</td>
<td width="60%">
The consumer is removing a counter from the query. PERFLIB calls the callback with this request code for each counter  being removed from the query. The  <i>Buffer</i> parameter contains a <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_identity">PERF_COUNTER_IDENTITY</a> structure that identifies the counter being removed.

Providers can use this notification to stop counting.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_ENUM_INSTANCES"></a><a id="perf_enum_instances"></a><dl>
<dt><b>PERF_ENUM_INSTANCES</b></dt>
</dl>
</td>
<td width="60%">
The consumer is  enumerating instances of the counter set. The <i>Buffer</i> parameter contains a null-terminated Unicode string that identifies the name of the computer (or its IP address) from which the consumer is enumerating the instances.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_COLLECT_START"></a><a id="perf_collect_start"></a><dl>
<dt><b>PERF_COLLECT_START</b></dt>
</dl>
</td>
<td width="60%">
The consumer is beginning to  collect counter data. The <i>Buffer</i> parameter contains a null-terminated Unicode string that identifies the name of the computer (or its IP address) from which the consumer is collecting data.

Providers can use this notification if the raw data state is critical (for example, transaction-related counters where partial updates are not allowed). This notification gives the provider a chance to flush all pending updates and lock future updates before collection begins.

</td>
</tr>
<tr>
<td width="40%"><a id="PERF_COLLECT_END"></a><a id="perf_collect_end"></a><dl>
<dt><b>PERF_COLLECT_END</b></dt>
</dl>
</td>
<td width="60%">
The counter data collection is complete.  The <i>Buffer</i> parameter contains a null-terminated Unicode string that identifies the name of the computer (or its IP address) from which the consumer collected data.

Providers can use this notification to release the update lock imposed by the collection start notification so that updates to the counter data can resume.

</td>
</tr>
</table>

### -param Buffer [in]

The contents of the buffer depends on the request. For possible content, see the <i>RequestCode</i> parameter.

### -param BufferSize [in]

Size, in bytes, of the <i>Buffer</i> parameter.

## -returns

Return ERROR_SUCCESS if the callback succeeds. 

If the callback fails, PERFLIB will return the error code to the consumer if the request is <b>PERF_ADD_COUNTER</b>, <b>PERF_ENUM_INSTANCES</b>, or <b>PERF_COLLECT_START</b>; otherwise, the error code is ignored.

## -remarks

If the <b>callback</b> attribute of the <a href="/previous-versions/aa373164(v=vs.85)">provider</a> element is "custom" or you used the <b>-NotificationCallback</b> argument when calling <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a>, you must implement this function. You pass the name of your callback function to <a href="/windows/desktop/PerfCtrs/counterinitialize">CounterInitialize</a>.

<b>Windows Vista:  </b>The <a href="/windows/desktop/PerfCtrs/counterinitialize">CounterInitialize</a> function is named <b>PerfAutoInitialize</b>. The <a href="/windows/desktop/PerfCtrs/ctrpp">CTRPP</a> tool also generates a skeleton of this callback for you that includes all the request codes. You then add code to the request codes that you want to support and remove the others.

The callback must complete within one second. If the callback does not complete in time, PERFLIB continues with the consumer's request and ignores the callback's return value when it completes.


#### Examples

The following example shows a simple implementation of a 
<a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> function.


```cpp
ULONG MyControlCallback(ULONG RequestCode, PVOID pBuffer, ULONG* pBufferSize)
{
    ULONG Status = ERROR_SUCCESS;
    PWNODE_HEADER Wnode = (PWNODE_HEADER)pBuffer;
    LPWSTR pComputerName = NULL;
    LPWSTR pInstance = NULL;
    PPERF_COUNTER_IDENTITY pCounter;
    UNREFERENCED_PARAMETER(pBufferSize);

    switch (RequestCode) 
    {
        case PERF_ADD_COUNTER:
            pCounter = (PPERF_COUNTER_IDENTITY)(((LPBYTE) Wnode) + sizeof(WNODE_HEADER));
            pComputerName = (LPWSTR)(((LPBYTE) pCounter) + pCounter->MachineOffset);
            pInstance = (pCounter->NameOffset > 0) 
                ? (LPWSTR) (((LPBYTE) pCounter) + pCounter->NameOffset) : NULL;
            
            break;

        case PERF_REMOVE_COUNTER: 
            pCounter = (PPERF_COUNTER_IDENTITY)(((LPBYTE) Wnode) + sizeof(WNODE_HEADER));
            pComputerName = (LPWSTR)(((LPBYTE) pCounter) + pCounter->MachineOffset);
            pInstance = (pCounter->NameOffset > 0)
                ? (LPWSTR) (((LPBYTE) pCounter) + pCounter->NameOffset) : NULL;
            
            break;

        case PERF_ENUM_INSTANCES:
            pComputerName = (LPWSTR) (((LPBYTE) Wnode) + sizeof(WNODE_HEADER));
            
            break;

        case PERF_COLLECT_START: 
            pComputerName = (LPWSTR) (((LPBYTE) Wnode) + sizeof(WNODE_HEADER));
            
            break;

        case PERF_COLLECT_END: 
            pComputerName = (LPWSTR) (((LPBYTE) Wnode) + sizeof(WNODE_HEADER));
            
            break;

        default:
            wprintf(L"Unknown request code, %lu\n", RequestCode);
    }

    return Status;
}

```