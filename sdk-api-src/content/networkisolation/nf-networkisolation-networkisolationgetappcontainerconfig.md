---
UID: NF:networkisolation.NetworkIsolationGetAppContainerConfig
title: NetworkIsolationGetAppContainerConfig function
author: windows-sdk-content
description: Is used to retrieve configuration information about one or more app containers.
old-location: ics\networkisolationgetappcontainerconfig.htm
tech.root: ICS
ms.assetid: 5ddb9dde-c989-4235-9784-af3168b7a151
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: NetworkIsolationGetAppContainerConfig, NetworkIsolationGetAppContainerConfig function [ICS/ICF], ics.networkisolationgetappcontainerconfig, networkisolation/NetworkIsolationGetAppContainerConfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: networkisolation.h
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetworkIsolationGetAppContainerConfig function


## -description


The <b>NetworkIsolationGetAppContainerConfig</b> function is used to retrieve configuration information about one or more app containers.


## -parameters




### -param pdwNumPublicAppCs [out]

Type: <b>DWORD*</b>

The number of app containers in the <b>appContainerSids</b> member.


### -param appContainerSids [out]

Type: <b><a href="https://msdn.microsoft.com/d15d5a3f-6b38-4b92-b59c-ff0d27d111d9">PSID_AND_ATTRIBUTES</a>*</b>

The security identifiers (SIDs) of app containers that are allowed to send loopback traffic. Used for debugging purposes.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 




## -remarks



Note that it is the calling program's responsibility to free the memory associated with the PSID_AND_ATTRIBUTES structure. The following code sample shows how to call this function. The FreeAppContainerConfig function shows how to free all of the associated memory.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#include "stdafx.h"
#include &lt;netfw.h&gt;

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

    for (dwIndex = 0; dwIndex &lt; sidCount; dwIndex++)
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
        &amp;dwCount, 
        &amp;appContainerSids
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
</pre>
</td>
</tr>
</table></span></div>


