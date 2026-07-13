---
UID: NF:rasdlg.RasDialDlgA
title: RasDialDlgA function (rasdlg.h)
description: The RasDialDlg function establishes a RAS connection using a specified phone-book entry and the credentials of the logged-on user. The function displays a stream of dialog boxes that indicate the state of the connection operation. (ANSI)
helpviewer_keywords: ["RasDialDlgA", "rasdlg/RasDialDlgA"]
old-location: rras\rasdialdlg.htm
tech.root: RRAS
ms.assetid: 698a18a1-b302-4b0d-8399-0bbdbe775f08
ms.date: 12/05/2018
ms.keywords: RasDialDlg, RasDialDlg function [RAS], RasDialDlgA, RasDialDlgW, _ras_rasdialdlg, rasdlg/RasDialDlg, rasdlg/RasDialDlgA, rasdlg/RasDialDlgW, rras.rasdialdlg
req.header: rasdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasDialDlgW (Unicode) and RasDialDlgA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasdlg.lib
req.dll: Rasdlg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasDialDlgA
 - rasdlg/RasDialDlgA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasdlg.dll
 - Ext-MS-Win-ras-rasdlg-l1-1-0.dll
api_name:
 - RasDialDlg
 - RasDialDlgA
 - RasDialDlgW
---

# RasDialDlgA function


## -description

The 
<b>RasDialDlg</b> function establishes a RAS connection using a specified phone-book entry and the credentials of the logged-on user. The function displays a stream of dialog boxes that indicate the state of the connection operation.

## -parameters

### -param lpszPhonebook [in]

Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.

### -param lpszEntry [in]

Pointer to a null-terminated string that specifies the name of the phone-book entry to dial.

### -param lpszPhoneNumber [in]

Pointer to a null-terminated string that specifies a phone number that overrides the numbers stored in the phone-book entry. If this parameter is <b>NULL</b>, 
<b>RasDialDlg</b> uses the numbers in the phone-book entry.

### -param lpInfo [in]

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)">RASDIALDLG</a> structure that specifies additional input and output parameters. The <b>dwSize</b> member of this structure must specify sizeof(<b>RASDIALDLG</b>). If an error occurs, the <b>dwError</b> member returns an error code; otherwise, it returns zero.

## -returns

If the function establishes a RAS connection, the return value is <b>TRUE</b>. Otherwise, the function should return <b>FALSE</b>.

If an error occurs, <b>RasDialDlg</b> should set the <b>dwError</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)">RASDIALDLG</a> structure to a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

## -remarks

The 
<b>RasDialDlg</b> function displays a series of dialog boxes that are similar to the dialog boxes the main <b>Dial-Up Networking</b> dialog box displays when the user selects the <b>Dial</b> button. Use the 
<b>RasDialDlg</b> function to display a standard user interface for a connection operation without presenting the main phone-book dialog box. For example, the RAS AutoDial service uses this function to establish a connection using the phone-book entry associated with a remote address.

The 
<b>RasDialDlg</b> function displays dialog boxes during the connection operation to provide feedback to the user about the progress of the operation. For example, the dialog boxes might indicate when the operation is dialing, when it is authenticating the user's credentials on the remote server, and so on. The dialog boxes also provide a <b>Cancel</b> button for the user to terminate the operation.

<b>RasDialDlg</b> returns when the connection is established, or when the user cancels the operation.

The following sample code dials the entry in the default phone-book specified by the variable <i>lpszEntry</i>.

<div class="alert"><b>Note</b>  This simple sample is intended to run on Windows Vista and later versions of Windows. Please be aware the call to sizeof(RASENTRY) will return a different value depending on what version of the operating system the code is being run. Please take steps to ensure this is handled appropriately.</div>
<div> </div>

```cpp
#include <windows.h>
#include <stdio.h>
#include "ras.h"
#include "rasdlg.h"
#include <tchar.h>
#include "strsafe.h"

#define PHONE_NUMBER_LENGTH 7
#define DEVICE_NAME_LENGTH 5
#define DEVICE_TYPE_LENGTH 5

DWORD __cdecl wmain(){

    DWORD dwError = ERROR_SUCCESS;
    BOOL nRet = TRUE;
    LPTSTR lpszEntry = L"EntryName";
    LPTSTR lpszphonenumber = L"5555555";
    LPTSTR lpszdevicename = L"Modem";
    LPTSTR lpszdevicetype = RASDT_Modem;

    // Allocate heap memory and initialize RASENTRY structure
    LPRASENTRY lpentry = (LPRASENTRY)HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, sizeof(RASENTRY));
    // Allocate heap memory and initialize RASDIALDLG structure
    LPRASDIALDLG lpInfo = (LPRASDIALDLG) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, sizeof(RASDIALDLG));
    
    if (lpentry == NULL || lpInfo == NULL){
        wprintf(L"HeapAlloc failed");
        HeapFree(GetProcessHeap(), 0, lpentry);
        HeapFree(GetProcessHeap(), 0, lpInfo);
        return 0;
    }

    // The RASDIALDLG and RASENTRY dwSize members have to be initialized or the RasDialDlg()
    // RasSetEntryProperties() APIs will fail below.
    lpInfo->dwSize = sizeof(RASDIALDLG);
    lpentry->dwSize = sizeof(RASENTRY);
    lpentry->dwFramingProtocol = RASFP_Ppp;
    lpentry->dwfOptions = 0;
    lpentry->dwType = RASFP_Ppp;
    dwError |= StringCchCopyN(lpentry->szLocalPhoneNumber, RAS_MaxPhoneNumber, lpszphonenumber, PHONE_NUMBER_LENGTH);
    dwError |= StringCchCopyN(lpentry->szDeviceName, RAS_MaxDeviceName, lpszdevicename, DEVICE_NAME_LENGTH);
    dwError |= StringCchCopyN(lpentry->szDeviceType, RAS_MaxDeviceType, lpszdevicetype, DEVICE_TYPE_LENGTH);
    
    if (dwError != S_OK){
        wprintf(L"Structure initialization failed: Error = %d\n", dwError);
        HeapFree(GetProcessHeap(), 0, lpentry);
        HeapFree(GetProcessHeap(), 0, lpInfo);
        return 0;
    }

    // Validate the new entry's name
    dwError = RasValidateEntryName(NULL, lpszEntry);
    if (dwError != ERROR_SUCCESS){
        wprintf(L"RasValidateEntryName failed: Error = %d\n", dwError);
        HeapFree(GetProcessHeap(), 0, lpentry);
        HeapFree(GetProcessHeap(), 0, lpInfo);
        return 0;
    }

    // Create and set the new entry's properties
    dwError = RasSetEntryProperties(NULL, lpszEntry, lpentry, lpentry->dwSize, NULL, 0);
    if (dwError != ERROR_SUCCESS){
        wprintf(L"RasSetEntryProperties failed: Error = %d\n", dwError);
        HeapFree(GetProcessHeap(), 0, lpentry);
        HeapFree(GetProcessHeap(), 0, lpInfo);
        return 0;
    }
    
    // Connect using the new entry
    nRet = RasDialDlg(NULL, lpszEntry, NULL, lpInfo);
    if (nRet != TRUE){
        wprintf(L"RasDialDlg failed: Error = %d\n", lpInfo->dwError);
    }
    
    // Clean up: delete the new entry
    dwError = RasDeleteEntry(NULL, lpszEntry);
    if (dwError != ERROR_SUCCESS){
        wprintf(L"RasDeleteEntry failed: Error = %d\n", dwError);
    }
    
    HeapFree(GetProcessHeap(), 0, lpentry);
    HeapFree(GetProcessHeap(), 0, lpInfo);

    return 0;
}

```






> [!NOTE]
> The rasdlg.h header defines RasDialDlg as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)">RASDIALDLG</a>



<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasphonebookdlga">RasPhonebookDlg</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
