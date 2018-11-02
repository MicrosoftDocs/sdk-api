---
UID: NF:evntrace.QueryAllTracesW
title: QueryAllTracesW function
author: windows-sdk-content
description: The QueryAllTraces function retrieves the properties and statistics for all event tracing sessions started on the computer for which the caller has permissions to query.
old-location: etw\queryalltraces.htm
tech.root: etw
ms.assetid: 6b6144b0-9152-4b5e-863d-06e823fbe084
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: QueryAllTraces, QueryAllTraces function [ETW], QueryAllTracesA, QueryAllTracesW, _evt_queryalltraces, base.queryalltraces, etw.queryalltraces, evntrace/QueryAllTraces, evntrace/QueryAllTracesA, evntrace/QueryAllTracesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryAllTracesW (Unicode) and QueryAllTracesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista and Windows XP
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista and Windows XP
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sechost.dll
 - Advapi32.dll
 - AdvApi32Legacy.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - API-MS-Win-Eventing-Legacy-l1-1-0.dll
 - KernelBase.dll
api_name:
 - QueryAllTraces
 - QueryAllTracesA
 - QueryAllTracesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QueryAllTracesW function


## -description


The <b>QueryAllTraces</b> function retrieves the properties 
   and statistics for all event tracing sessions started on the computer for which the caller has permissions to 
   query.


## -parameters




### -param PropertyArray [out]

An array of pointers to 
       <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structures that receive 
       session properties and statistics for the event tracing sessions.

You only need to set the <b>Wnode.BufferSize</b>, 
       <b>LoggerNameOffset</b> , and <b>LogFileNameOffset</b>  members of the 
       <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure. The other 
       members should all be set to zero.


### -param PropertyArrayCount [in]

Number of structures in the <i>PropertyArray</i> array. This value must be less than or 
      equal to 64, the maximum number of event tracing sessions that ETW supports.


### -param LoggerCount

TBD




#### - SessionCount [out]

Actual number of event tracing sessions started on the computer. 


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>. The following table includes some 
       common errors and their causes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true:

<ul>
<li><i>PropertyArrayCount</i> is zero or greater than the maximum number of supported sessions</li>
<li><i>PropertyArray</i> is <b>NULL</b></li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The property array is too small to receive information for all sessions 
        (<i>SessionCount</i> is greater than <i>PropertyArrayCount</i>). The 
        function fills the property array with the number of property structures specified in 
        <i>PropertyArrayCount</i>.

</td>
</tr>
</table>
 




## -remarks



Event trace controllers call this function.

This function retrieves the trace sessions that the caller has permissions to query. Users running with 
    elevated administrative privileges, users in the Performance Log Users group, and services running as LocalSystem, 
    LocalService, NetworkService can view all tracing sessions.

This function does not return private logging sessions.

To retrieve information for a single session, use the 
    <a href="https://msdn.microsoft.com/c39f669c-ff40-40ed-ba47-798474ec2de4">ControlTrace</a> function and set the 
    <i>ControlCode</i> parameter to <b>EVENT_TRACE_CONTROL_QUERY</b>.


#### Examples

The following example shows how to call this function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;wmistr.h&gt;
#include &lt;evntrace.h&gt;

#define MAX_SESSIONS 64
#define MAX_SESSION_NAME_LEN 1024
#define MAX_LOGFILE_PATH_LEN 1024

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    PEVENT_TRACE_PROPERTIES pSessions[MAX_SESSIONS];    // Array of pointers to property structures
    PEVENT_TRACE_PROPERTIES pBuffer = NULL;             // Buffer that contains all the property structures
    ULONG SessionCount = 0;                             // Actual number of sessions started on the computer
    ULONG BufferSize = 0;
    ULONG PropertiesSize = 0;
    WCHAR SessionGuid[50];


    // The size of the session name and log file name used by the
    // controllers are not known, therefore create a properties structure that allows
    // for the maximum size of both.

    PropertiesSize = sizeof(EVENT_TRACE_PROPERTIES) +
        (MAX_SESSION_NAME_LEN*sizeof(WCHAR)) +
        (MAX_LOGFILE_PATH_LEN*sizeof(WCHAR));

    BufferSize = PropertiesSize * MAX_SESSIONS;

    pBuffer = (PEVENT_TRACE_PROPERTIES) malloc(BufferSize);

    if (pBuffer)
    {
        ZeroMemory(pBuffer, BufferSize);

        for (USHORT i = 0; i &lt; MAX_SESSIONS; i++)
        {
            pSessions[i] = (EVENT_TRACE_PROPERTIES*)((BYTE*)pBuffer + (i*PropertiesSize));
            pSessions[i]-&gt;Wnode.BufferSize = PropertiesSize;
            pSessions[i]-&gt;LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
            pSessions[i]-&gt;LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) + (MAX_SESSION_NAME_LEN*sizeof(WCHAR));
        }
    }
    else
    {
        wprintf(L"Error allocating memory for properties.\n");
        goto cleanup;
    }

    status = QueryAllTraces(pSessions, (ULONG)MAX_SESSIONS, &amp;SessionCount);

    if (ERROR_SUCCESS == status || ERROR_MORE_DATA == status)
    {
        wprintf(L"Requested session count, %d. Actual session count, %d.\n\n", MAX_SESSIONS, SessionCount);

        for (USHORT i = 0; i &lt; SessionCount; i++)
        {
            StringFromGUID2(pSessions[i]-&gt;Wnode.Guid, SessionGuid, (sizeof(SessionGuid) / sizeof(SessionGuid[0])));

                wprintf(L"Session GUID: %s\nSession ID: %d\nSession name: %s\nLog file: %s\n"
                    L"min buffers: %d\nmax buffers: %d\nbuffers: %d\nbuffers written: %d\n"
                    L"buffers lost: %d\nevents lost: %d\n\n",
                    SessionGuid,
                    pSessions[i]-&gt;Wnode.HistoricalContext,
                    (LPWSTR)((char*)pSessions[i] + pSessions[i]-&gt;LoggerNameOffset),
                    (LPWSTR)((char*)pSessions[i] + pSessions[i]-&gt;LogFileNameOffset),
                    pSessions[i]-&gt;MinimumBuffers,
                    pSessions[i]-&gt;MaximumBuffers,
                    pSessions[i]-&gt;NumberOfBuffers,
                    pSessions[i]-&gt;BuffersWritten,
                    pSessions[i]-&gt;LogBuffersLost,
                    pSessions[i]-&gt;EventsLost);
        }
    }
    else
    {
        wprintf(L"Error calling QueryAllTraces, %d.\n", status);
        goto cleanup;
    }

cleanup:

    if (pBuffer)
    {
        free(pBuffer);
        pBuffer = NULL;
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c39f669c-ff40-40ed-ba47-798474ec2de4">ControlTrace</a>



<a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a>



<a href="https://msdn.microsoft.com/9a9e2f53-9916-4a9c-a08e-c8affd5fc4c9">EnumerateTraceGuids</a>
 

 

