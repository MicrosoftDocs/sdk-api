---
UID: NF:evntrace.QueryAllTracesA
title: QueryAllTracesA function (evntrace.h)
description: The QueryAllTracesA (ANSI) function (evntrace.h) function retrieves the properties and statistics for all event tracing sessions that the caller can query.
helpviewer_keywords:
  [
    "QueryAllTraces",
    "QueryAllTraces function [ETW]",
    "QueryAllTracesA",
    "QueryAllTracesW",
    "_evt_queryalltraces",
    "base.queryalltraces",
    "etw.queryalltraces",
    "evntrace/QueryAllTraces",
    "evntrace/QueryAllTracesA",
    "evntrace/QueryAllTracesW",
  ]
old-location: etw\queryalltraces.htm
tech.root: ETW
ms.assetid: 6b6144b0-9152-4b5e-863d-06e823fbe084
ms.date: 08/04/2022
ms.keywords:
  QueryAllTraces, QueryAllTraces function [ETW], QueryAllTracesA,
  QueryAllTracesW, _evt_queryalltraces, base.queryalltraces, etw.queryalltraces,
  evntrace/QueryAllTraces, evntrace/QueryAllTracesA, evntrace/QueryAllTracesW
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
req.lib:
  Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - QueryAllTracesA
  - evntrace/QueryAllTracesA
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
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
---

# QueryAllTracesA function

## -description

The **QueryAllTraces** function retrieves the properties and statistics for all
event tracing sessions for which the caller has permissions to query.

## -parameters

### -param PropertyArray [out]

An array of pointers to
[EVENT_TRACE_PROPERTIES](/windows/desktop/ETW/event-trace-properties) structures
that receive session properties and statistics for the event tracing sessions.

You only need to set the **Wnode.BufferSize**, **LoggerNameOffset** , and
**LogFileNameOffset** members of the
[EVENT_TRACE_PROPERTIES](/windows/desktop/ETW/event-trace-properties) structure.
The other members should all be set to zero.

### -param PropertyArrayCount [in]

Number of structures in the _PropertyArray_ array. This value must be less than
or equal to 64, the maximum number of event tracing sessions that ETW supports.

**Windows 10:** _PropertyArrayCount_ may be larger than 64 and some systems may
support more than 64 tracing sessions.

### -param LoggerCount [out]

Receives the number of traces for which data is returned. This may differ from
the actual number of running event tracing sessions running if the caller does
not have permissions to query all sessions.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
are some common errors and their causes.

- **ERROR_INVALID_PARAMETER**

  One of the following is true:

  - _PropertyArrayCount_ is zero or greater than the maximum number of supported
    sessions
  - _PropertyArray_ is **NULL**

- **ERROR_MORE_DATA**

  The property array is too small to receive information for all sessions
  (_SessionCount_ is greater than _PropertyArrayCount_). The function fills the
  property array with the number of property structures specified in
  _PropertyArrayCount_.

## -remarks

Event trace controllers call this function.

This function retrieves the trace sessions that the caller has permissions to
query. Users running with elevated administrative privileges, users in the
Performance Log Users group, and services running as LocalSystem, LocalService,
NetworkService can view most tracing sessions.

This function does not return private logging sessions.

To retrieve information for a single session, use the
[ControlTrace](/windows/desktop/ETW/controltrace) function and set the
_ControlCode_ parameter to **EVENT_TRACE_CONTROL_QUERY**.

### Examples

The following example shows how to call this function.

```cpp
#include <windows.h>
#include <evntrace.h>
#include <vector>

const unsigned MAX_SESSION_NAME_LEN = 1024;
const unsigned MAX_LOGFILE_PATH_LEN = 1024;
const unsigned PropertiesSize =
    sizeof(EVENT_TRACE_PROPERTIES) +
    (MAX_SESSION_NAME_LEN * sizeof(WCHAR)) +
    (MAX_LOGFILE_PATH_LEN * sizeof(WCHAR));

int wmain()
{
    ULONG status;
    std::vector<EVENT_TRACE_PROPERTIES*> sessions; // Array of pointers to property structures
    std::vector<BYTE> buffer;                      // Buffer that contains all the property structures
    ULONG sessionCount;                            // Actual number of sessions started on the computer

    // The size of the session name and log file name used by the
    // controllers are not known, therefore create a properties structure that allows
    // for the maximum size of both.

    try
    {
        sessionCount = 64; // Start with room for 64 sessions.
        do
        {
            sessions.resize(sessionCount);
            buffer.resize(PropertiesSize * sessionCount);

            for (size_t i = 0; i != sessions.size(); i += 1)
            {
                sessions[i] = (EVENT_TRACE_PROPERTIES*)&buffer[i * PropertiesSize];
                sessions[i]->Wnode.BufferSize = PropertiesSize;
                sessions[i]->LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
                sessions[i]->LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) + (MAX_SESSION_NAME_LEN * sizeof(WCHAR));
            }

            status = QueryAllTracesW(&sessions[0], sessionCount, &sessionCount);
        } while (status == ERROR_MORE_DATA);

        if (status != ERROR_SUCCESS)
        {
            printf("Error calling QueryAllTraces: %u\n", status);
        }
        else
        {
            printf("Actual session count: %u.\n\n", sessionCount);

            for (ULONG i = 0; i < sessionCount; i++)
            {
                WCHAR sessionGuid[50];
                (void)StringFromGUID2(sessions[i]->Wnode.Guid, sessionGuid, ARRAYSIZE(sessionGuid));

                printf(
                    "Session GUID: %ls\n"
                    "Session ID: %llu\n"
                    "Session name: %ls\n"
                    "Log file: %ls\n"
                    "min buffers: %u\n"
                    "max buffers: %u\n"
                    "buffers: %u\n"
                    "buffers written: %u\n"
                    "buffers lost: %u\n"
                    "events lost: %u\n"
                    "\n",
                    sessionGuid,
                    sessions[i]->Wnode.HistoricalContext,
                    (PCWSTR)((LPCBYTE)sessions[i] + sessions[i]->LoggerNameOffset),
                    (PCWSTR)((LPCBYTE)sessions[i] + sessions[i]->LogFileNameOffset),
                    sessions[i]->MinimumBuffers,
                    sessions[i]->MaximumBuffers,
                    sessions[i]->NumberOfBuffers,
                    sessions[i]->BuffersWritten,
                    sessions[i]->LogBuffersLost,
                    sessions[i]->EventsLost);
            }
        }
    }
    catch (std::bad_alloc const&)
    {
        printf("Error allocating memory for properties.\n");
        status = ERROR_OUTOFMEMORY;
    }

    return status;
}
```

> [!NOTE]
> The evntrace.h header defines QueryAllTraces as an alias which
> automatically selects the ANSI or Unicode version of this function based on
> the definition of the UNICODE preprocessor constant. Mixing usage of the
> encoding-neutral alias with code that not encoding-neutral can lead to
> mismatches that result in compilation or runtime errors. For more information,
> see
> [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[ControlTrace](/windows/desktop/ETW/controltrace)

[EVENT_TRACE_PROPERTIES](/windows/desktop/ETW/event-trace-properties)

[EnumerateTraceGuids](/windows/desktop/ETW/enumeratetraceguids)
