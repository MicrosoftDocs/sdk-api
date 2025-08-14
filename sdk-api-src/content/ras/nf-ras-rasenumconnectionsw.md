---
UID: NF:ras.RasEnumConnectionsW
title: RasEnumConnectionsW function (ras.h)
description: The RasEnumConnections function lists all active RAS connections. It returns each connection's handle and phone-book entry name. (Unicode)
helpviewer_keywords: ["RasEnumConnections", "RasEnumConnections function [RAS]", "RasEnumConnectionsW", "_ras_rasenumconnections", "ras/RasEnumConnections", "ras/RasEnumConnectionsW", "rras.rasenumconnections"]
old-location: rras\rasenumconnections.htm
tech.root: RRAS
ms.assetid: b581cfbf-a55e-4f56-89cd-168aa23af550
ms.date: 12/05/2018
ms.keywords: RasEnumConnections, RasEnumConnections function [RAS], RasEnumConnectionsA, RasEnumConnectionsW, _ras_rasenumconnections, ras/RasEnumConnections, ras/RasEnumConnectionsA, ras/RasEnumConnectionsW, rras.rasenumconnections
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasEnumConnectionsW (Unicode) and RasEnumConnectionsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasEnumConnectionsW
 - ras/RasEnumConnectionsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-rasapi32-l1-1-2.dll
 - Rasapi32.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasEnumConnections
 - RasEnumConnectionsA
 - RasEnumConnectionsW
---

# RasEnumConnectionsW function


## -description

The 
<b>RasEnumConnections</b> function lists all active RAS connections. It returns each connection's handle and phone-book entry name.

## -parameters

### -param unnamedParam1 [in, out]

Pointer to a buffer that receives, on output, an array of 
<a href="/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)">RASCONN</a> structures, one for each RAS connection. 




On input, an application must set the <b>dwSize</b> member of the first 
<a href="/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)">RASCONN</a> structure in the buffer to sizeof(<b>RASCONN</b>) in order to identify the version of the structure being passed.

### -param unnamedParam2 [in, out]

Pointer to a variable that, on input, contains the size, in bytes, of the buffer specified by <i>lprasconn</i>. 




On output, the function sets this variable to the number of bytes required to enumerate the RAS connections.

<div class="alert"><b>Note</b>  <p class="note">To determine the required buffer size, call 
<b>RasEnumConnections</b> with <i>lprasconn</i> set to <b>NULL</b>. The variable pointed to by <i>lpcb</i> should be set to zero. The function will return the required buffer size in <i>lpcb</i> and an error code of <b>ERROR_BUFFER_TOO_SMALL</b>.

</div>
<div> </div>

### -param unnamedParam3 [out]

Pointer to a variable that receives the number of 
<a href="/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)">RASCONN</a> structures written to the buffer specified by <i>lprasconn</i>.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>lprasconn</i> buffer is not large enough. The <i>lpcb</i> parameter is less than the <b>dwSize</b> member in the <i>lprasconn</i> parameter which is should be set prior to calling the function. The function returns the required buffer size in the variable pointed to by <i>lpcb</i>.

</td>
</tr>
</table>

## -remarks

If a connection was made without specifying a phone-book entry name, the information returned for that connection gives the connection phone number preceded by ".".

The following code sample code uses <b>RasEnumConnections</b> to enumerates the active RAS connections.


```cpp
#include <windows.h>
#include <stdio.h>
#include "ras.h"
#include "raserror.h"
#pragma comment(lib, "rasapi32.lib")

DWORD __cdecl wmain(){

    DWORD dwCb = 0;
    DWORD dwRet = ERROR_SUCCESS;
    DWORD dwConnections = 0;
    LPRASCONN lpRasConn = NULL;
    
    // Call RasEnumConnections with lpRasConn = NULL. dwCb is returned with the required buffer size and 
    // a return code of ERROR_BUFFER_TOO_SMALL
    dwRet = RasEnumConnections(lpRasConn, &dwCb, &dwConnections);

    if (dwRet == ERROR_BUFFER_TOO_SMALL){
        // Allocate the memory needed for the array of RAS structure(s).
        lpRasConn = (LPRASCONN) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, dwCb);
        if (lpRasConn == NULL){
            wprintf(L"HeapAlloc failed!\n");
            return 0;
        }
        // The first RASCONN structure in the array must contain the RASCONN structure size
        lpRasConn[0].dwSize = sizeof(RASCONN);
        
        // Call RasEnumConnections to enumerate active connections
        dwRet = RasEnumConnections(lpRasConn, &dwCb, &dwConnections);

        // If successful, print the names of the active connections.
        if (ERROR_SUCCESS == dwRet){
            wprintf(L"The following RAS connections are currently active:\n");
            for (DWORD i = 0; i < dwConnections; i++){
                         wprintf(L"%s\n", lpRasConn[i].szEntryName);
                  }
        }
        //Deallocate memory for the connection buffer
        HeapFree(GetProcessHeap(), 0, lpRasConn);
        lpRasConn = NULL;
        return 0;
    }

    // There was either a problem with RAS or there are no connections to enumerate    
    if(dwConnections >= 1){
        wprintf(L"The operation failed to acquire the buffer size.\n");
    }else{
        wprintf(L"There are no active RAS connections.\n");
    }

    return 0;
}

```


<b>RasEnumConnections</b> cannot  enumerate a connection as <b>Active</b> until RAS has successfully connected. 

<b>Windows Me/98/95:  </b><b>RasEnumConnections</b>  enumerates a connection as <b>Active</b> as soon as it starts dialing.

The most reliable way to enumerate and check for an active connection is to call <b>RasEnumConnections</b> or <a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> to get a connection handle, then call <a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a> to determine the actual connection state.







> [!NOTE]
> The ras.h header defines RasEnumConnections as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)">RASCONN</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumentriesa">RasEnumEntries</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
