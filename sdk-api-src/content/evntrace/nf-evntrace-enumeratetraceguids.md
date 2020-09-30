---
UID: NF:evntrace.EnumerateTraceGuids
title: EnumerateTraceGuids function (evntrace.h)
description: The EnumerateTraceGuids function retrieves information about registered event trace providers that are running on the computer.
helpviewer_keywords: ["EnumerateTraceGuids","EnumerateTraceGuids function [ETW]","_evt_enumeratetraceguids","base.enumeratetraceguids","etw.enumeratetraceguids","evntrace/EnumerateTraceGuids"]
old-location: etw\enumeratetraceguids.htm
tech.root: ETW
ms.assetid: 9a9e2f53-9916-4a9c-a08e-c8affd5fc4c9
ms.date: 12/05/2018
ms.keywords: EnumerateTraceGuids, EnumerateTraceGuids function [ETW], _evt_enumeratetraceguids, base.enumeratetraceguids, etw.enumeratetraceguids, evntrace/EnumerateTraceGuids
req.header: evntrace.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumerateTraceGuids
 - evntrace/EnumerateTraceGuids
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-eventing-Legacy-l1-1-0.dll
 - advapi32legacy.dll
api_name:
 - EnumerateTraceGuids
---

# EnumerateTraceGuids function


## -description

The 
<b>EnumerateTraceGuids</b> function retrieves information about registered event trace providers that are running on the computer. 
		
<div class="alert"><b>Note</b>  This function has been superseded by <a href="/windows/desktop/ETW/enumeratetraceguidsex">EnumerateTraceGuidsEx</a>.</div><div> </div>

## -parameters

### -param GuidPropertiesArray [in, out]

An array of pointers to 
<a href="/windows/desktop/ETW/trace-guid-properties">TRACE_GUID_PROPERTIES</a> structures.

### -param PropertyArrayCount [in]

Number of elements in the <i>GuidPropertiesArray</i> array.

### -param GuidCount [out]

Actual number of event tracing providers registered on the computer.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some common errors and their causes.

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
<li><i>PropertyArrayCount</i> is zero</li>
<li><i>GuidPropertiesArray</i> is <b>NULL</b></li>
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
The property array is too small to receive information for all registered providers (<i>GuidCount</i> is greater than <i>PropertyArrayCount</i>). The function fills the GUID property array with the number of structures specified in <i>PropertyArrayCount</i>.

</td>
</tr>
</table>

## -remarks

Event trace controllers call this function.

For information on registering event trace providers, see 
<a href="/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a>.

You can use the <a href="/windows/desktop/ETW/trace-guid-properties">TRACE_GUID_PROPERTIES.LoggerId</a> member to determine which session enabled the provider if <b>TRACE_GUID_PROPERTIES.IsEnable</b> is <b>TRUE</b>.

The list will not include kernel providers.


#### Examples

The following example shows you how to call this function.


```cpp
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

#define MAX_SESSION_NAME_LEN 1024
#define MAX_LOGFILE_PATH_LEN 1024

BOOL IsPrivateSession(DWORD SessionId);

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    PTRACE_GUID_PROPERTIES pProviderProperties = NULL; // Buffer that contains the block of property structures
    PTRACE_GUID_PROPERTIES *pProviders = NULL;         // Array of pointers to property structures in ProviderProperties
    PTRACE_GUID_PROPERTIES *pTemp = NULL;
    ULONG RegisteredProviderCount = 0;                 // Actual number of providers registered on the computer
    ULONG ProviderCount = 0;
    ULONG EnabledProviderCount = 0;
    ULONG BufferSize = 0;
    WCHAR ProviderGuid[50];

    // EnumerateTraceGuids requires a valid pointer. Create a dummy
    // allocation, so that you can get the actual allocation size.

    pProviders = (PTRACE_GUID_PROPERTIES *) malloc(sizeof(PTRACE_GUID_PROPERTIES));

    if (NULL == pProviders)
    {
        wprintf(L"Error allocating memory for dummy pProviders allocation.\n");
        goto cleanup;
    }

    // Pass zero for the array size to get the number of registered providers 
    // for this snapshot. Then allocate memory for the block of structures
    // and the array of pointers.

    status = EnumerateTraceGuids(pProviders, ProviderCount, &RegisteredProviderCount);

    if (ERROR_MORE_DATA == status)
    {
        ProviderCount = RegisteredProviderCount;

        BufferSize = sizeof(TRACE_GUID_PROPERTIES) * RegisteredProviderCount;

        pProviderProperties = (PTRACE_GUID_PROPERTIES) malloc(BufferSize);

        if (NULL == pProviderProperties)
        {
            wprintf(L"Error allocating memory for properties.\n");
            goto cleanup;
        }

        ZeroMemory(pProviderProperties, BufferSize);

        pTemp = (PTRACE_GUID_PROPERTIES *) realloc(pProviders, RegisteredProviderCount * sizeof(PTRACE_GUID_PROPERTIES));

        if (NULL == pTemp)
        {
            wprintf(L"Error allocating memory for pProviders allocation.\n");
            goto cleanup;
        }

        pProviders = pTemp;
        pTemp = NULL;

        for (USHORT i = 0; i < RegisteredProviderCount; i++)
        {
            pProviders[i] = &pProviderProperties[i];
        }

        status = EnumerateTraceGuids(pProviders, ProviderCount, &RegisteredProviderCount);

        if (ERROR_SUCCESS == status || ERROR_MORE_DATA == status)
        {
            for (USHORT i=0; i < RegisteredProviderCount; i++)
            {
                StringFromGUID2(pProviders[i]->Guid, ProviderGuid, sizeof(ProviderGuid)),

                wprintf(L"Provider: %s\nEnabled: %s\n",
                    ProviderGuid,
                    (pProviders[i]->IsEnable) ? L"TRUE" : L"FALSE");

                if (pProviders[i]->IsEnable)
                {
                    EnabledProviderCount++;

                    wprintf(L"Session ID: %ld\nPrivate Session: %s\n"
                        L"Enable level: %ld\nEnable flags: %ld\n",
                        pProviders[i]->LoggerId,
                        (IsPrivateSession(pProviders[i]->LoggerId)) ? L"TRUE" : L"FALSE",
                        pProviders[i]->EnableLevel,
                        pProviders[i]->EnableFlags);
                }
      
                wprintf(L"\n");
            }

            wprintf(L"\nRegistered provider count is %lu; %lu of which are enabled.\n", 
                RegisteredProviderCount, EnabledProviderCount);
        }
        else
        {
            wprintf(L"Error calling EnumerateTraceGuids, %d.\n", status);
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"Error calling EnumerateTraceGuids to get allocation size, %d.\n", status);
        goto cleanup;
    }

cleanup:

    if (pProviders)
    {
        free(pProviders);
    }

    if (pProviderProperties)
    {
        free(pProviderProperties);
    }
}


BOOL IsPrivateSession(DWORD SessionId)
{
    DWORD status = ERROR_SUCCESS;
    BOOL IsPrivate = FALSE;
    PEVENT_TRACE_PROPERTIES pProperties;
    ULONG BufferSize = 0;

    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) +
        (MAX_SESSION_NAME_LEN*sizeof(WCHAR)) +
        (MAX_LOGFILE_PATH_LEN*sizeof(WCHAR));

    pProperties = (PEVENT_TRACE_PROPERTIES) malloc(BufferSize);

    if (pProperties)
    {
        ZeroMemory(pProperties, BufferSize);

        pProperties->Wnode.BufferSize = BufferSize;
        pProperties->LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
        pProperties->LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) + (MAX_SESSION_NAME_LEN*sizeof(WCHAR));
    }
    else
    {
        wprintf(L"Error allocating memory for properties.\n");
        goto cleanup;
    }

    status = ControlTrace((TRACEHANDLE)SessionId, NULL, pProperties, EVENT_TRACE_CONTROL_QUERY);

    if (ERROR_SUCCESS == status)
    {
        if ((EVENT_TRACE_PRIVATE_LOGGER_MODE & pProperties->LogFileMode)== EVENT_TRACE_PRIVATE_LOGGER_MODE)
        {
            IsPrivate = TRUE;
        }
    }
    else if (ERROR_WMI_INSTANCE_NOT_FOUND == status)
    {
        wprintf(L"The session is no longer running\n");
    }
    else
    {
        wprintf(L"ControlTrace(QUERY) failed with %lu\n", status);
    }

cleanup:

    if (pProperties)
    {
        free(pProperties);
        pProperties = NULL;
    }

    return IsPrivate;
}

```

## -see-also

<a href="/windows/desktop/ETW/enumeratetraceguidsex">EnumerateTraceGuidsEx</a>



<a href="/windows/desktop/ETW/queryalltraces">QueryAllTraces</a>



<a href="/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a>



<a href="/windows/desktop/ETW/trace-guid-properties">TRACE_GUID_PROPERTIES</a>