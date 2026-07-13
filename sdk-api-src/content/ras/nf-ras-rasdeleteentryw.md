---
UID: NF:ras.RasDeleteEntryW
title: RasDeleteEntryW function (ras.h)
description: The RasDeleteEntry function deletes an entry from a phone book. (Unicode)
helpviewer_keywords: ["RasDeleteEntry", "RasDeleteEntry function [RAS]", "RasDeleteEntryW", "_ras_rasdeleteentry", "ras/RasDeleteEntry", "ras/RasDeleteEntryW", "rras.rasdeleteentry"]
old-location: rras\rasdeleteentry.htm
tech.root: RRAS
ms.assetid: 80a6c2d3-917b-4d13-867f-a1399d434105
ms.date: 12/05/2018
ms.keywords: RasDeleteEntry, RasDeleteEntry function [RAS], RasDeleteEntryA, RasDeleteEntryW, _ras_rasdeleteentry, ras/RasDeleteEntry, ras/RasDeleteEntryA, ras/RasDeleteEntryW, rras.rasdeleteentry
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasDeleteEntryW (Unicode) and RasDeleteEntryA (ANSI)
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
 - RasDeleteEntryW
 - ras/RasDeleteEntryW
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
 - RasDeleteEntry
 - RasDeleteEntryA
 - RasDeleteEntryW
---

# RasDeleteEntryW function


## -description

The 
<b>RasDeleteEntry</b> function deletes an entry from a phone book.

## -parameters

### -param unnamedParam1 [in]

 Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box. 




<b>Windows Me/98/95:  </b>This parameter should always be <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.

### -param unnamedParam2 [in]

Pointer to a null-terminated string that specifies the name of an existing entry to be deleted.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have correct privileges. Only an administrator can complete this task.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The entry name specified in <i>lpszEntry</i> does not exist.

</td>
</tr>
</table>

## -remarks

The following sample code deletes the phone-book entry specified by the variable <i>lpszEntry</i>.


```cpp
#include <stdio.h>
#include <windows.h>
#include "ras.h"
#include "strsafe.h"

#define PHONE_NUMBER_LENGTH 7
#define DEVICE_NAME_LENGTH 5
#define DEVICE_TYPE_LENGTH 5

DWORD __cdecl wmain(){

    DWORD dwRet = ERROR_SUCCESS;
    LPTSTR lpszEntry = L"RASEntryName";
    LPTSTR lpszphonenumber = L"5555555";
    LPTSTR lpszdevicename = L"Modem";
    LPTSTR lpszdevicetype = RASDT_Modem;

    // Allocate heap memory for the RASENTRY structure
    LPRASENTRY lpentry = (LPRASENTRY)HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, sizeof(RASENTRY));
    if (lpentry == NULL){
        printf("HeapAlloc failed");
        return 0;
       }
  
    // The RASENTRY->dwSize member has to be initialized or the RRAS APIs will fail below.
    lpentry->dwSize = sizeof(RASENTRY);
    lpentry->dwFramingProtocol = RASFP_Ppp;
    lpentry->dwfOptions = 0;
    lpentry->dwType = RASET_Phone;
    dwRet |= StringCchCopyN(lpentry->szLocalPhoneNumber, RAS_MaxPhoneNumber, lpszphonenumber, PHONE_NUMBER_LENGTH);
    dwRet |= StringCchCopyN(lpentry->szDeviceName, RAS_MaxDeviceName, lpszdevicename, DEVICE_NAME_LENGTH);
    dwRet |= StringCchCopyN(lpentry->szDeviceType, RAS_MaxDeviceType, lpszdevicetype, DEVICE_TYPE_LENGTH);
    if (dwRet != ERROR_SUCCESS){
        wprintf(L"RASENTRY structure initialization failed");
        HeapFree(GetProcessHeap(), 0, lpentry);
        return 0;
    }

    // Validate the new entry's name
    dwRet = RasValidateEntryName(NULL, lpszEntry);
    if (dwRet != ERROR_SUCCESS){
        wprintf(L"RasValidateEntryName failed: Error = %d\n", dwRet);
        HeapFree(GetProcessHeap(), 0, lpentry);
        return 0;
    }

    // Create and set the new entry's properties
    dwRet = RasSetEntryProperties(NULL, lpszEntry, lpentry, lpentry->dwSize, NULL, 0);
    if (dwRet != ERROR_SUCCESS){
        wprintf(L"RasSetEntryProperties failed: Error = %d\n", dwRet);
        HeapFree(GetProcessHeap(), 0, lpentry);
        return 0;
    }

    // Clean up: delete the new entry
    dwRet = RasDeleteEntry(NULL, lpszEntry);
    if (dwRet != ERROR_SUCCESS){
        wprintf(L"RasDeleteEntry failed: Error = %d\n", dwRet);
    }

    HeapFree(GetProcessHeap(), 0, lpentry);
    return 0;
}

```






> [!NOTE]
> The ras.h header defines RasDeleteEntry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ras/nf-ras-rascreatephonebookentrya">RasCreatePhonebookEntry</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumentriesa">RasEnumEntries</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
