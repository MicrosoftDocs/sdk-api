---
UID: NF:ras.RasEnumConnectionsA
title: RasEnumConnectionsA function
author: windows-sdk-content
description: The RasEnumConnections function lists all active RAS connections. It returns each connection's handle and phone-book entry name.
old-location: rras\rasenumconnections.htm
tech.root: RRAS
ms.assetid: b581cfbf-a55e-4f56-89cd-168aa23af550
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RasEnumConnections, RasEnumConnections function [RAS], RasEnumConnectionsA, RasEnumConnectionsW, _ras_rasenumconnections, ras/RasEnumConnections, ras/RasEnumConnectionsA, ras/RasEnumConnectionsW, rras.rasenumconnections
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasEnumConnections
 - RasEnumConnectionsA
 - RasEnumConnectionsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasEnumConnectionsA function


## -description


The 
<b>RasEnumConnections</b> function lists all active RAS connections. It returns each connection's handle and phone-book entry name.


## -parameters




### -param arg1 [in, out]

Pointer to a buffer that receives, on output, an array of 
<a href="https://msdn.microsoft.com/234834e2-f539-42de-add7-63e93086de17">RASCONN</a> structures, one for each RAS connection. 




On input, an application must set the <b>dwSize</b> member of the first 
<a href="https://msdn.microsoft.com/234834e2-f539-42de-add7-63e93086de17">RASCONN</a> structure in the buffer to sizeof(<b>RASCONN</b>) in order to identify the version of the structure being passed.


### -param arg2 [in, out]

Pointer to a variable that, on input, contains the size, in bytes, of the buffer specified by <i>lprasconn</i>. 




On output, the function sets this variable to the number of bytes required to enumerate the RAS connections.

<div class="alert"><b>Note</b>  <p class="note">To determine the required buffer size, call 
<b>RasEnumConnections</b> with <i>lprasconn</i> set to <b>NULL</b>. The variable pointed to by <i>lpcb</i> should be set to zero. The function will return the required buffer size in <i>lpcb</i> and an error code of <b>ERROR_BUFFER_TOO_SMALL</b>.

</div>
<div> </div>

### -param arg3 [out]

Pointer to a variable that receives the number of 
<a href="https://msdn.microsoft.com/234834e2-f539-42de-add7-63e93086de17">RASCONN</a> structures written to the buffer specified by <i>lprasconn</i>.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

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
The <i>lprasconn</i> buffer is not large enough. The <i>lpcb</i>parameter is less than the <b>dwSize</b> member in the <i>lprasconn</i>parameter which is should be set prior to calling the function. The function returns the required buffer size in the variable pointed to by <i>lpcb</i>.

</td>
</tr>
</table>
 




## -remarks



If a connection was made without specifying a phone-book entry name, the information returned for that connection gives the connection phone number preceded by ".".

The following code sample code uses <b>RasEnumConnections</b> to enumerates the active RAS connections.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
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
    dwRet = RasEnumConnections(lpRasConn, &amp;dwCb, &amp;dwConnections);

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
        dwRet = RasEnumConnections(lpRasConn, &amp;dwCb, &amp;dwConnections);

        // If successful, print the names of the active connections.
        if (ERROR_SUCCESS == dwRet){
            wprintf(L"The following RAS connections are currently active:\n");
            for (DWORD i = 0; i &lt; dwConnections; i++){
                         wprintf(L"%s\n", lpRasConn[i].szEntryName);
                  }
        }
        //Deallocate memory for the connection buffer
        HeapFree(GetProcessHeap(), 0, lpRasConn);
        lpRasConn = NULL;
        return 0;
    }

    // There was either a problem with RAS or there are no connections to enumerate    
    if(dwConnections &gt;= 1){
        wprintf(L"The operation failed to acquire the buffer size.\n");
    }else{
        wprintf(L"There are no active RAS connections.\n");
    }

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>
<b>RasEnumConnections</b> cannot  enumerate a connection as <b>Active</b> until RAS has successfully connected. 

<b>Windows Me/98/95:  </b><b>RasEnumConnections</b>  enumerates a connection as <b>Active</b> as soon as it starts dialing.

      The most reliable way to enumerate and check for an active connection is to call <b>RasEnumConnections</b> or <a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> to get a connection handle, then call <a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a> to determine the actual connection state.






## -see-also




<a href="https://msdn.microsoft.com/234834e2-f539-42de-add7-63e93086de17">RASCONN</a>



<a href="https://msdn.microsoft.com/9df7402f-c93e-45d4-925a-f2ce9d547bce">RasEnumEntries</a>



<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

