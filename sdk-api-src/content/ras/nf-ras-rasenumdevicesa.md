---
UID: NF:ras.RasEnumDevicesA
title: RasEnumDevicesA function (ras.h)
description: The RasEnumDevices function returns the name and type of all available RAS-capable devices. (ANSI)
helpviewer_keywords: ["RasEnumDevicesA", "ras/RasEnumDevicesA"]
old-location: rras\rasenumdevices.htm
tech.root: RRAS
ms.assetid: 819f069f-15e7-41b6-9153-4d602be4245d
ms.date: 12/05/2018
ms.keywords: RasEnumDevices, RasEnumDevices function [RAS], RasEnumDevicesA, RasEnumDevicesW, _ras_rasenumdevices, ras/RasEnumDevices, ras/RasEnumDevicesA, ras/RasEnumDevicesW, rras.rasenumdevices
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasEnumDevicesW (Unicode) and RasEnumDevicesA (ANSI)
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
 - RasEnumDevicesA
 - ras/RasEnumDevicesA
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
 - RasEnumDevices
 - RasEnumDevicesA
 - RasEnumDevicesW
---

# RasEnumDevicesA function


## -description

The 
<b>RasEnumDevices</b> function returns the name and type of all available RAS-capable devices.

## -parameters

### -param unnamedParam1 [in]

Pointer to a buffer that receives an array of 
<a href="/previous-versions/windows/desktop/legacy/aa377001(v=vs.85)">RASDEVINFO</a> structures, one for each RAS-capable device. Before calling the function, set the <b>dwSize</b> member of the first 
<b>RASDEVINFO</b> structure in the buffer to sizeof(<b>RASDEVINFO</b>) to identify the version of the structure.

### -param unnamedParam2 [in, out]

Pointer to a variable that, on input, contains the size, in bytes, of the <i>lpRasDevInfo</i> buffer. 




On output, the function sets this variable to the number of bytes required to enumerate the devices.

<div class="alert"><b>Note</b>  <p class="note">To determine the required buffer size, call 
<b>RasEnumDevices</b> with <i>lpRasDevInfo</i> set to <b>NULL</b>. The variable pointed to by <i>lpcb</i> should be set to zero. The function will return the required buffer size in <i>lpcb</i> and an error code of <b>ERROR_BUFFER_TOO_SMALL</b>.

</div>
<div> </div>

### -param unnamedParam3 [out]

Pointer to a variable that receives the number of 
<a href="/previous-versions/windows/desktop/legacy/aa377001(v=vs.85)">RASDEVINFO</a> structures written to the <i>lpRasDevInfo</i> buffer.

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
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpRasDevInfo</i> buffer is not large enough. The <i>lpcb</i> parameter is less than the <b>dwSize</b> member in the <i>lpRasDevInfo</i> parameter which should be set prior to calling the function. The function returns the required buffer size in the variable pointed to by <i>lpcb</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates insufficient memory. The <i>lpRasDevInfo</i> parameter is non-<b>NULL</b>, the <i>lpcb</i> parameter is non-<b>NULL</b> and an internal memory allocation failed. This is possibly due to a low-memory condition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Indicates an invalid parameter value. The <i>lpcb</i> parameter is <b>NULL</b> or the <i>lpcDevices</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The address or buffer specified by <i>lpRasDevInfo</i> is invalid. The <b>dwSize</b> member of the 
								<i>lpRasDevInfo</i>  parameter does not equal sizeof(<a href="/previous-versions/windows/desktop/legacy/aa377001(v=vs.85)">RASDEVINFO</a>).

</td>
</tr>
</table>

## -remarks

The following sample code enumerates the devices on the current machine. The code initially calls 
<b>RasEnumDevices</b> with a <i>lpRasDevInfo</i> parameter of <b>NULL</b>, to obtain the size of the buffer that should be passed in. The code also sets the <b>dwSize</b> member of the first 
<a href="/previous-versions/windows/desktop/legacy/aa377001(v=vs.85)">RASDEVINFO</a> structure to sizeof(<b>RASDEVINFO</b>) to specify the version of the structure.


```cpp
#include <windows.h>
#include <stdio.h>
#include "ras.h"
#include "raserror.h"
#pragma comment(lib, "rasapi32.lib")

DWORD __cdecl wmain(){

    DWORD dwCb = 0;
    DWORD dwRet = ERROR_SUCCESS;
    DWORD dwDevices = 0;
    LPRASDEVINFO lpRasDevInfo = NULL;
    
    // Call RasEnumDevices with lpRasDevInfo = NULL. dwCb is returned with the required buffer size and 
    // a return code of ERROR_BUFFER_TOO_SMALL
    dwRet = RasEnumDevices(lpRasDevInfo, &dwCb, &dwDevices);

    if (dwRet == ERROR_BUFFER_TOO_SMALL){
        // Allocate the memory needed for the array of RAS structure(s).
        lpRasDevInfo = (LPRASDEVINFO) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, dwCb);
        if (lpRasDevInfo == NULL){
            wprintf(L"HeapAlloc failed!\n");
            return 0;
        }
        // The first RASDEVINFO structure in the array must contain the structure size
        lpRasDevInfo[0].dwSize = sizeof(RASDEVINFO);
        
        // Call RasEnumDevices to enumerate RAS devices
        dwRet = RasEnumDevices(lpRasDevInfo, &dwCb, &dwDevices);

        // If successful, print the names of the RAS devices
        if (ERROR_SUCCESS == dwRet){
            wprintf(L"The following RAS devices were found:\n");
            for (DWORD i = 0; i < dwDevices; i++){
                         wprintf(L"%s\n", lpRasDevInfo[i].szDeviceName);
                  }
        }
        //Deallocate memory for the connection buffer
        HeapFree(GetProcessHeap(), 0, lpRasDevInfo);
        lpRasDevInfo = NULL;
        return 0;
    }

    // There was either a problem with RAS or there are no RAS devices to enumerate    
    if(dwDevices >= 1){
        wprintf(L"The operation failed to acquire the buffer size.\n");
    }else{
        wprintf(L"There were no RAS devices found.\n");
    }

    return 0;
}

```






> [!NOTE]
> The ras.h header defines RasEnumDevices as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377001(v=vs.85)">RASDEVINFO</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
