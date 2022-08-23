---
UID: NF:netfw.NetworkIsolationGetAppContainerConfig
title: NetworkIsolationGetAppContainerConfig function (netfw.h)
description: The NetworkIsolationGetAppContainerConfig function is used to retrieve configuration information about one or more app containers.
helpviewer_keywords: ["NetworkIsolationGetAppContainerConfig","NetworkIsolationGetAppContainerConfig function [ICS/ICF]","ics.networkisolationgetappcontainerconfig","networkisolation/NetworkIsolationGetAppContainerConfig"]
old-location: ics\networkisolationgetappcontainerconfig.htm
tech.root: ics
ms.assetid: 5ddb9dde-c989-4235-9784-af3168b7a151
ms.date: 08/02/2022
ms.keywords: NetworkIsolationGetAppContainerConfig, NetworkIsolationGetAppContainerConfig function [ICS/ICF], ics.networkisolationgetappcontainerconfig, networkisolation/NetworkIsolationGetAppContainerConfig
req.header: netfw.h
req.include-header: Netfw.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Firewallapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetworkIsolationGetAppContainerConfig
 - netfw/NetworkIsolationGetAppContainerConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - firewallapi.dll
 - API-MS-Win-Net-Isolation-l1-1-0.dll
 - API-MS-Win-Net-Isolation-l1-1-1.dll
 - wfapihost.dll
api_name:
 - NetworkIsolationGetAppContainerConfig
---

# NetworkIsolationGetAppContainerConfig function


## -description

The <b>NetworkIsolationGetAppContainerConfig</b> function is used to retrieve configuration information about one or more app containers.

## -parameters

### -param pdwNumPublicAppCs [out]

Type: <b>DWORD*</b>

The number of app containers in the <b>appContainerSids</b> member.

### -param appContainerSids [out]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">PSID_AND_ATTRIBUTES</a>*</b>

The security identifiers (SIDs) of app containers that are allowed to send loopback traffic. Used for debugging purposes.

## -returns

Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.

## -remarks

Note that it is the calling program's responsibility to free the memory associated with the PSID_AND_ATTRIBUTES structure. The following code sample shows how to call this function. The FreeAppContainerConfig function shows how to free all of the associated memory.


```cpp

#include "stdafx.h"
#include <netfw.h>

typedef DWORD
(WINAPI *FN_NETWORKISOLATIONGETAPPCONTAINERCONFIG)(
    _Out_ DWORD *pdwNumPublicAppCs,
    _Outptr_result_buffer_(*pdwNumPublicAppCs) PSID_AND_ATTRIBUTES *appContainerSids
    );

void
FreeAppContainerConfig(
    __in DWORD sidCount,
    __in_ecount(sidCount) SID_AND_ATTRIBUTES *srcSidAttrib
    )
{
    DWORD dwIndex = 0;

    for (dwIndex = 0; dwIndex < sidCount; dwIndex++)
    {
        HeapFree(GetProcessHeap(), 0, srcSidAttrib[dwIndex].Sid);
    }

    HeapFree(GetProcessHeap(), 0, srcSidAttrib);
}

int _tmain(int argc, _TCHAR* argv[])
{
    DWORD dwErr = 0;
    PSID_AND_ATTRIBUTES appContainerSids = NULL;
    DWORD dwCount = 0;
    HMODULE hModule = NULL;
    FN_NETWORKISOLATIONGETAPPCONTAINERCONFIG pfnNetworkIsolationGetAppContainerConfig = NULL;

    hModule = LoadLibraryW(L"FirewallAPI.dll");
    if (hModule == NULL)
    {
        dwErr = GetLastError();
        goto Cleanup;
    }

    pfnNetworkIsolationGetAppContainerConfig = (FN_NETWORKISOLATIONGETAPPCONTAINERCONFIG)GetProcAddress(
        hModule, 
        "NetworkIsolationGetAppContainerConfig"
        );
    if (pfnNetworkIsolationGetAppContainerConfig == NULL)
    {
        dwErr = GetLastError();
        goto Cleanup;
    }

    dwErr = pfnNetworkIsolationGetAppContainerConfig(
        &dwCount, 
        &appContainerSids
        );
    if (dwErr != ERROR_SUCCESS)
    {
        goto Cleanup;
    }

    // Process the app container sids

Cleanup:

    FreeAppContainerConfig(
        dwCount, 
        appContainerSids
        );

    if (hModule != NULL)
    {
        FreeLibrary(hModule);
    }

	return 0;
}

```
