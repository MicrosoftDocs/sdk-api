---
UID: NF:ras.RasEnumAutodialAddressesA
title: RasEnumAutodialAddressesA function (ras.h)
description: The RasEnumAutodialAddresses function returns a list of all addresses in the AutoDial mapping database. (ANSI)
helpviewer_keywords: ["RasEnumAutodialAddressesA", "ras/RasEnumAutodialAddressesA"]
old-location: rras\rasenumautodialaddresses.htm
tech.root: RRAS
ms.assetid: bd4fb897-5cc0-452f-b6a2-ec0540c59b90
ms.date: 12/05/2018
ms.keywords: RasEnumAutodialAddresses, RasEnumAutodialAddresses function [RAS], RasEnumAutodialAddressesA, RasEnumAutodialAddressesW, _ras_rasenumautodialaddresses, ras/RasEnumAutodialAddresses, ras/RasEnumAutodialAddressesA, ras/RasEnumAutodialAddressesW, rras.rasenumautodialaddresses
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasEnumAutodialAddressesW (Unicode) and RasEnumAutodialAddressesA (ANSI)
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
 - RasEnumAutodialAddressesA
 - ras/RasEnumAutodialAddressesA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasEnumAutodialAddresses
 - RasEnumAutodialAddressesA
 - RasEnumAutodialAddressesW
---

# RasEnumAutodialAddressesA function


## -description

The 
<b>RasEnumAutodialAddresses</b> function returns a list of all addresses in the AutoDial mapping database.

## -parameters

### -param lppRasAutodialAddresses [in, out]

Pointer to an array of string pointers, with additional space for the storage of the strings themselves at the end of the buffer. 




On output, each string receives the name of an address in the AutoDial mapping database.

If <i>lppAddresses</i> is <b>NULL</b> on input, 
<b>RasEnumAutodialAddresses</b> sets the <i>lpdwcbAddresses</i> and <i>lpdwcAddresses</i> parameters to indicate the required size, in bytes, and the number of address entries in the database.

### -param lpdwcbRasAutodialAddresses [in, out]

Pointer to a variable that, on input, contains the size, in bytes, of the buffer specified by the <i>lpRasEnumAutodialAddressespAddresses</i> parameter. 




<div class="alert"><b>Note</b>  <p class="note">To determine the required buffer size, call 
<b>RasEnumAutodialAddresses</b> with <i>lppAddresses</i> set to <b>NULL</b>. The variable pointed to by <i>lpdwcbAddresses</i> should be set to zero. The function will return the required buffer size in <i>lpdwcbAddresses</i> and an error code of <b>ERROR_BUFFER_TOO_SMALL</b>.

</div>
<div> </div>

### -param lpdwcRasAutodialAddresses [out]

Pointer to a variable that receives the number of address strings returned in the <i>lppAddresses</i> buffer.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> was passed for the <i>lpdwcbAddresses</i> or <i>lpdwcAddresses</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>lppAddresses</i> buffer was <b>NULL</b> and <i>lpdwcbAddresses</i> was zero. The function returns the required buffer size in the variable pointed to by <i>lpdwcbAddresses</i>.

</td>
</tr>
</table>

## -remarks

The following code sample code uses <b>RasEnumAutodialAddresses</b> to enumerate the Autodial mapping database.


```cpp
#include <windows.h>
#include <stdio.h>
#include "ras.h"
#include "raserror.h"
#include <tchar.h>

DWORD __cdecl wmain(){

    DWORD dwBytes = 0;
    DWORD dwRet = ERROR_SUCCESS;
    DWORD dwAddresses = 0;
    LPTSTR * lppAddresses = NULL;
    LPCTSTR lpEntryAddress = L"www.microsoft.com";

    // Allocate memory for a new Autodial address to add to the mapping database
    LPRASAUTODIALENTRY lpentry = (LPRASAUTODIALENTRY) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, sizeof(RASAUTODIALENTRY));
    lpentry->dwSize = sizeof(RASAUTODIALENTRY);

    // Add a (non-functional) address to the Autodial mapping database
    // (this ensures RasEnumAutodialAddresses() has something to return)
    dwRet = RasSetAutodialAddress(lpEntryAddress, 0, lpentry, lpentry->dwSize, 1);
    
    // Call RasEnumAutodialAddresses() with lppAddresses = NULL. dwBytes is returned with the 
    // required buffer size and a return code of ERROR_BUFFER_TOO_SMALL
    dwRet = RasEnumAutodialAddresses(lppAddresses, &dwBytes, &dwAddresses);

    if (dwRet == ERROR_BUFFER_TOO_SMALL){
        // Allocate the memory needed for the array of RAS Autodial addresses.
        lppAddresses = (LPTSTR *) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, dwBytes);
        if (lppAddresses == NULL){
            wprintf(L"HeapAlloc failed!\n");
            return 0;
        }
        
        // Call RasEnumAutodialAddresses() to enumerate all RAS Autodial addresses
        dwRet = RasEnumAutodialAddresses(lppAddresses, &dwBytes, &dwAddresses);

        // If successful, print the RAS Autodial addresses
        if (dwRet == ERROR_SUCCESS){
            wprintf(L"The following RAS Autodial addresses were found:\n");
            for (DWORD i = 0; i < dwAddresses; i++){
                wprintf(L"%s\n", lppAddresses[i]);
            }
        }
        // Remove the address
        dwRet = RasSetAutodialAddress(lpEntryAddress, 0, NULL, 0, 0);
        
        //Deallocate memory for the address buffers
        HeapFree(GetProcessHeap(), 0, lppAddresses);    
        HeapFree(GetProcessHeap(), 0, lpentry);
        lppAddresses = NULL;
        return 0;
    }

    // There was either a problem with RAS or there are no RAS Autodial addresses to enumerate
    if(dwAddresses >= 1){
        wprintf(L"The operation failed to acquire the buffer size.\n");
    }else{
        wprintf(L"There were no RAS Autodial addresses found.\n");
    }

    // Remove the address
    dwRet = RasSetAutodialAddress(lpEntryAddress, 0, NULL, 0, 0);
    HeapFree(GetProcessHeap(), 0, lpentry);
    return 0;
}

```






> [!NOTE]
> The ras.h header defines RasEnumAutodialAddresses as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)">RASAUTODIALENTRY</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetautodialaddressa">RasGetAutodialAddress</a>



<a href="/windows/desktop/api/ras/nf-ras-rassetautodialaddressa">RasSetAutodialAddress</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
