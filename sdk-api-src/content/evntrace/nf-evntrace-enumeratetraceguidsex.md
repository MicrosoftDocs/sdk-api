---
UID: NF:evntrace.EnumerateTraceGuidsEx
title: EnumerateTraceGuidsEx function (evntrace.h)
description: Use this function to retrieve information about trace providers that are registered on the computer.
helpviewer_keywords: ["EnumerateTraceGuidsEx","EnumerateTraceGuidsEx function [ETW]","base.enumeratetraceguidsex","etw.enumeratetraceguidsex","evntrace/EnumerateTraceGuidsEx"]
old-location: etw\enumeratetraceguidsex.htm
tech.root: ETW
ms.assetid: 9d70fe21-1750-4d60-a825-2004f7d666c7
ms.date: 12/05/2018
ms.keywords: EnumerateTraceGuidsEx, EnumerateTraceGuidsEx function [ETW], base.enumeratetraceguidsex, etw.enumeratetraceguidsex, evntrace/EnumerateTraceGuidsEx
f1_keywords:
- evntrace/EnumerateTraceGuidsEx
dev_langs:
- c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
- sechost.dll
- API-MS-Win-eventing-controller-l1-1-0.dll
- kernelbase.dll
api_name:
- EnumerateTraceGuidsEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EnumerateTraceGuidsEx function


## -description


Use this function to retrieve information about trace providers that are registered on the computer.


## -parameters




### -param TraceQueryInfoClass [in]

Determines the type of information to include with the list of registered providers. For possible values, see the <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-info-class">TRACE_QUERY_INFO_CLASS</a> enumeration.


### -param InBuffer [in]

GUID of the provider or provider group whose information you want to retrieve. Specify the GUID only if <i>TraceQueryInfoClass</i> is <b>TraceGuidQueryInfo</b> or <b>TraceGroupQueryInfo</b>.


### -param InBufferSize [in]

Size, in bytes, of the data <i>InBuffer</i>.


### -param OutBuffer [out]

Application-allocated buffer that contains the enumerated information. The format of the information depends on the value of <i>TraceQueryInfoClass</i>. For details, see Remarks.


### -param OutBufferSize [in]

Size, in bytes, of the <i>OutBuffer</i> buffer. If the function succeeds, the <i>ReturnLength</i> parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and the <i>ReturnLength</i> parameter receives the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and the <i>ReturnLength</i> parameter receives the required buffer size.


### -param ReturnLength [out]

Actual size of the data in <i>OutBuffer</i>, in bytes.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some common errors and their causes.

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
One of the parameters is not valid. 



								
							

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>OutBuffer</i> buffer is too small to receive information for all registered providers. Reallocate the buffer using the size returned in <i>ReturnLength</i>.

</td>
</tr>
</table>
 




## -remarks



Event trace controllers call this function.

If <i>TraceQueryInfoClass</i> is <b>TraceGuidQueryInfo</b>, ETW returns the data in a <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-guid-info">TRACE_GUID_INFO</a> block that is a header to the information. The info block contains a <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-provider-instance-info">TRACE_PROVIDER_INSTANCE_INFO</a> block for each provider that uses the same GUID. Each instance info block contains a <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-enable-info">TRACE_ENABLE_INFO</a> structure for each session that enabled the provider.

For information on registering event trace providers, see 
<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a> and <a href="https://docs.microsoft.com/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a>.


#### Examples

The following example shows you how to call this function.


```cpp
#include <windows.h>
#include <stdio.h>
#include <evntcons.h>

DWORD GetProviderInfo(GUID ProviderGuid, PTRACE_GUID_INFO & pInfo);

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    GUID *pTemp = NULL;
    GUID *pGuids = NULL;
    DWORD GuidListSize = 0;
    DWORD GuidCount = 0;
    DWORD RequiredListSize = 0;
    WCHAR ProviderGuid[50];
    PTRACE_GUID_INFO pInfo = NULL;
    PTRACE_PROVIDER_INSTANCE_INFO pInstance = NULL;
    PTRACE_ENABLE_INFO pEnable = NULL;


    // Get the required buffer size for the query.

    status = EnumerateTraceGuidsEx(TraceGuidQueryList, NULL, 0, pGuids, GuidListSize, &RequiredListSize);

    // The number of registered providers could change between the 
    // time you called to get the buffer size and the time you called
    // to get the actual data, so call EnumerateTraceGuidsEx in a loop
    // until you no longer get ERROR_INSUFFICIENT_BUFFER.

    while (ERROR_INSUFFICIENT_BUFFER == status)
    {
        pTemp = (GUID *) realloc(pGuids, RequiredListSize);

        if (NULL == pTemp)
        {
            wprintf(L"Error allocating memory for list of provider GUIDs.\n");
            goto cleanup;
        }

        pGuids = pTemp;
        pTemp = NULL;

        GuidListSize = RequiredListSize;

        ZeroMemory(pGuids, GuidListSize);

        status = EnumerateTraceGuidsEx(TraceGuidQueryList, NULL, 0, pGuids, GuidListSize, &RequiredListSize);
    }

    if (ERROR_SUCCESS == status)
    {
        GuidCount = GuidListSize / sizeof(GUID);

        // For each registered provider on the computer, get information
        // about how it was registered. If a session enabled the
        // provider, get information on how the session enabled the provider.

        for (USHORT i = 0; i < GuidCount; i++)
        {
            StringFromGUID2(pGuids[i], ProviderGuid, sizeof(ProviderGuid)),

            wprintf(L"Provider: %s\n", ProviderGuid);

            status = GetProviderInfo(pGuids[i], pInfo);

            if (ERROR_SUCCESS == status)
            {
                pInstance = (PTRACE_PROVIDER_INSTANCE_INFO)((PBYTE)pInfo + sizeof(TRACE_GUID_INFO));

                if (pInfo->InstanceCount > 1)
                {
                    wprintf(L"There are %d providers that use the same GUID.\n", pInfo->InstanceCount);
                }

                for (DWORD j = 0; j < pInfo->InstanceCount; j++)
                {
                    wprintf(L"\tThe PID of the process that registered the provider is %lu.\n", pInstance->Pid);

                    if ((pInstance->Flags & TRACE_PROVIDER_FLAG_PRE_ENABLE) == TRACE_PROVIDER_FLAG_PRE_ENABLE)
                    {
                        wprintf(L"\tThe provider is not registered; however, one or more sessions have enabled the provider.\n");
                    }
                    else
                    {
                        if ((pInstance->Flags & TRACE_PROVIDER_FLAG_LEGACY) == TRACE_PROVIDER_FLAG_LEGACY)
                        {
                            wprintf(L"\tThe provider used RegisterTraceGuids to register itself.\n");
                        }
                        else
                        {
                            wprintf(L"\tThe provider used EventRegister to register itself.\n");
                        }
                    }

                    if (pInstance->EnableCount > 0)
                    {
                        wprintf(L"\tThe provider is enabled to the following sessions.\n");

                        pEnable = (PTRACE_ENABLE_INFO)((PBYTE)pInstance + sizeof(TRACE_PROVIDER_INSTANCE_INFO));

                        for (DWORD k = 0; k < pInstance->EnableCount; k++)
                        {
                            wprintf(L"\t\tSession Id: %hu\n", pEnable->LoggerId);
                            wprintf(L"\t\tLevel used to enable the provider: %hu\n", pEnable->Level);
                            wprintf(L"\t\tMatchAnyKeyword value used to enable the provider: %I64u\n", pEnable->MatchAnyKeyword);
                            wprintf(L"\t\tMatchAllKeyword value used to enable the provider: %I64u\n", pEnable->MatchAllKeyword);

                            if (pEnable->EnableProperty > 0)
                            {
                                wprintf(L"\t\tThe session requested that the following information be included with each event:\n");

                                if ((pEnable->EnableProperty & EVENT_ENABLE_PROPERTY_SID) == EVENT_ENABLE_PROPERTY_SID)
                                {
                                    wprintf(L"\t\t\tThe SID of the user that logged the event\n");
                                }

                                if ((pEnable->EnableProperty & EVENT_ENABLE_PROPERTY_TS_ID) == EVENT_ENABLE_PROPERTY_TS_ID)
                                {
                                    wprintf(L"\t\t\tThe terminal session ID\n");
                                }
                            }

                            pEnable++;

                            wprintf(L"\n");
                        }
                    }

                    pInstance = (PTRACE_PROVIDER_INSTANCE_INFO)((PBYTE)pInstance + pInstance->NextOffset);

                    wprintf(L"\n");
                }

                wprintf(L"\n");
            }
            else
            {
                wprintf(L"Error retrieving provider info (%lu)\n\n", status);
            }
        }

        wprintf(L"\nRegistered provider count is %lu.\n", GuidCount);
    }
    else
    {
        wprintf(L"EnumerateTraceGuidsEx(TraceGuidQueryList) failed with %lu.\n", status);
        goto cleanup;
    }

cleanup:

    if (pGuids)
    {
        free(pGuids);
        pGuids = NULL;
    }

    if (pInfo)
    {
        free(pInfo);
        pInfo = NULL;
    }
}


// Get information about the specified provider.

DWORD GetProviderInfo(GUID ProviderGuid, PTRACE_GUID_INFO & pInfo)
{
    ULONG status = ERROR_SUCCESS;
    PTRACE_GUID_INFO pTemp = NULL;
    DWORD InfoListSize = 0;
    DWORD RequiredListSize = 0;

    status = EnumerateTraceGuidsEx(TraceGuidQueryInfo, &ProviderGuid, sizeof(GUID), pInfo, InfoListSize, &RequiredListSize);

    while (ERROR_INSUFFICIENT_BUFFER == status)
    {
        pTemp = (PTRACE_GUID_INFO) realloc(pInfo, RequiredListSize);

        if (NULL == pTemp)
        {
            wprintf(L"Error allocating memory for provider info.\n");
            goto cleanup;
        }

        pInfo = pTemp;
        pTemp = NULL;

        InfoListSize = RequiredListSize;

        ZeroMemory(pInfo, InfoListSize);

        status = EnumerateTraceGuidsEx(TraceGuidQueryInfo, &ProviderGuid, sizeof(GUID), pInfo, InfoListSize, &RequiredListSize);
    }

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"EnumerateTraceGuidsEx(TraceGuidQueryInfo) failed with %lu.\n", status);
    }

cleanup:

    return status;
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/trace-info-class">TRACE_QUERY_INFO_CLASS</a>
 

 

