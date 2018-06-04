---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


