---
UID: NF:ras.RasGetCredentialsA
title: RasGetCredentialsA function (ras.h)
description: The RasGetCredentials function retrieves the user credentials associated with a specified RAS phone-book entry. (ANSI)
helpviewer_keywords: ["RasGetCredentialsA", "ras/RasGetCredentialsA"]
old-location: rras\rasgetcredentials.htm
tech.root: RRAS
ms.assetid: 37b67845-dd9f-4adc-a33a-f0e5c0bdb6f7
ms.date: 12/05/2018
ms.keywords: RasGetCredentials, RasGetCredentials function [RAS], RasGetCredentialsA, RasGetCredentialsW, _ras_rasgetcredentials, ras/RasGetCredentials, ras/RasGetCredentialsA, ras/RasGetCredentialsW, rras.rasgetcredentials
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetCredentialsW (Unicode) and RasGetCredentialsA (ANSI)
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
 - RasGetCredentialsA
 - ras/RasGetCredentialsA
dev_langs:
 - c++
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
 - RasGetCredentials
 - RasGetCredentialsA
 - RasGetCredentialsW
---

# RasGetCredentialsA function


## -description

The 
<b>RasGetCredentials</b> function retrieves the user credentials associated with a specified RAS phone-book entry.

## -parameters

### -param unnamedParam1 [in]

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.

### -param unnamedParam2 [in]

Pointer to a <b>null</b>-terminated string that specifies the name of a phone-book entry.

### -param unnamedParam3 [in, out]

Pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)">RASCREDENTIALS</a> structure that, on output, receives the user credentials associated with the specified phone-book entry. 




On input, set the <b>dwSize</b> member of the structure to sizeof(<a href="/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)">RASCREDENTIALS</a>), and set the <b>dwMask</b> member to indicate the credential information to retrieve. When the function returns, <b>dwMask</b> indicates the members that were successfully retrieved.

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
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
The specified phone book cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
The specified entry does not exist in the phone book.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpCredentials</i> parameter was <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwSize</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)">RASCREDENTIALS</a> structure is an unrecognized value.

</td>
</tr>
</table>

## -remarks

The 
<b>RasGetCredentials</b> function retrieves the credentials of the last user in order to connect using the specified phone-book entry, or the credentials subsequently specified in a call to the 
<a href="/windows/desktop/api/ras/nf-ras-rassetcredentialsa">RasSetCredentials</a> function for the phone-book entry.

 This function is the preferred way of securely retrieving the credentials associated with a RAS phone-book entry. 
<b>RasGetCredentials</b> supersedes the 
<a href="/windows/desktop/api/ras/nf-ras-rasgetentrydialparamsa">RasGetEntryDialParams</a> function, which may not be supported in future releases of Windows.

<b>RasGetCredentials</b> does not return the actual password. Instead, the <b>szPassword</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)">RASCREDENTIALS</a> structure contains a handle to the saved password. Substitute this handle for the saved password in subsequent calls to 
<a href="/windows/desktop/api/ras/nf-ras-rassetcredentialsa">RasSetCredentials</a> and 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>. When presented with this handle, 
<b>RasDial</b>  retrieves and uses the saved password. The value of this handle may change in future versions of the operating system; do not develop code that depends on the contents or format of this value.

The <b>dwMask</b> member of 
<a href="/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)">RASCREDENTIALS</a> contains the RASCM_Password flag if the system has saved a password for the specified entry. If the system has no password saved for this entry, <b>dwMask</b> does not contain RASCM_Password.

<b>Windows 2000/NT:  </b>This feature is not supported.

If the <b>dwMask</b> of the 
<a href="/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)">RASCREDENTIALS</a> structure contains the RASCM_DefaultCreds flag, the credentials returned are the default credentials for an all-user connection.

To retrieve a pre-shared key, use the RASCM_PreSharedKey flag in the RASCREDENTIALS.dwMask field.

<b>Windows 2000/NT:  </b>This feature is not supported.

The following sample code creates the "RasEntryName" phone book entry, sets its credentials using <a href="/windows/desktop/api/ras/nf-ras-rassetcredentialsa">RasSetCredentials</a>, and then retrieves those credentials using <b>RasGetCredentials</b>.


```cpp
#include <windows.h>
#include "ras.h"
#include <stdio.h>
#include <tchar.h>
#include "strsafe.h"

#define PHONE_NUMBER_LENGTH 7
#define DEVICE_NAME_LENGTH 5
#define DEVICE_TYPE_LENGTH 5
#define DOMAIN_NAME_LENGTH 9
#define USER_NAME_LENGTH 11

DWORD __cdecl wmain(){

    DWORD dwRet = ERROR_SUCCESS;    
    LPTSTR lpszEntry = L"RasEntryName";
    LPTSTR lpszPhoneNumber = L"5555555";
    LPTSTR lpszDeviceName = L"Modem";
    LPTSTR lpszDeviceType = RASDT_Modem;
    LPTSTR lpszDomainName = L"RASDomain";
    LPTSTR lpszUserName = L"RASUserName";
    /***********************************************************************************************/
    // Create a new phone book entry
    /***********************************************************************************************/
  
    // Allocate heap memory for the RASENTRY structure
    LPRASENTRY lpentry = (LPRASENTRY)HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, sizeof(RASENTRY));
    if (lpentry == NULL){
        wprintf(L"HeapAlloc failed!\n");
        return 0;
    }
    // The RASENTRY->dwSize member has to be initialized or the RRAS RasValidateEntryName() and 
    // RasSetEntryProperties APIs will fail below.
    lpentry->dwSize = sizeof(RASENTRY);
    lpentry->dwFramingProtocol = RASFP_Ppp;
    lpentry->dwfOptions = 0;
    lpentry->dwType = RASFP_Ppp;
    dwRet |= StringCchCopyN(lpentry->szLocalPhoneNumber, RAS_MaxPhoneNumber, lpszPhoneNumber, PHONE_NUMBER_LENGTH);
    dwRet |= StringCchCopyN(lpentry->szDeviceName, RAS_MaxDeviceName, lpszDeviceName, DEVICE_NAME_LENGTH);
    dwRet |= StringCchCopyN(lpentry->szDeviceType, RAS_MaxDeviceType, lpszDeviceType, DEVICE_TYPE_LENGTH);
    if (dwRet != ERROR_SUCCESS){
        wprintf(L"RASENTRY structure initialization failed!\n");
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

    /******************************************************************************************/
    // Set and get the new entry's credentials
    /******************************************************************************************/

    // Allocate heap memory for the RASCREDENTIALS structure
    LPRASCREDENTIALS lpCred = (LPRASCREDENTIALS) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, sizeof(RASCREDENTIALS));
    if (lpCred == NULL){
        wprintf(L"HeapAlloc failed!\n");
        return 0;
    }
    // The RASCREDENTIALS->dwsize member must be initialized or the RRAS RasSetCredentials() and 
    // RasGetCredentials() APIs will fail below
    lpCred->dwSize = sizeof(RASCREDENTIALS);

    // The entry's credentials must first be set with RasSetCredentials() before they can be 
    // retrieved with RasGetCredentials(). The values below are used to set the new entry's credentials.
    dwRet |= StringCchCopyN(lpCred->szDomain, DNLEN, lpszDomainName, DOMAIN_NAME_LENGTH);
    dwRet |= StringCchCopyN(lpCred->szUserName, UNLEN, lpszUserName, USER_NAME_LENGTH);
    if (dwRet != ERROR_SUCCESS){
        wprintf(L"RASCREDENTIALS structure initialization failed!\n");
        HeapFree(GetProcessHeap(), 0, lpCred);
        return 0;
    }
    // The username, password, and Domain credentials are valid
    lpCred->dwMask = RASCM_UserName | RASCM_Password | RASCM_Domain;
    
    // Set the newly created entry's credentials
    dwRet = RasSetCredentials(NULL, lpszEntry, lpCred, FALSE);
    
    // The same RASCREDENTIALS structure is used to 'set' and 'get' the credentials. Therefore, zero out 
    // its values. (this proves RasGetCredentials works below!) 
    dwRet |= StringCchCopyN(lpCred->szDomain, DNLEN, L"", 0);
    dwRet |= StringCchCopyN(lpCred->szUserName, UNLEN, L"", 0);
    dwRet |= StringCchCopyN(lpCred->szPassword, UNLEN, L"", 0);
    if (dwRet != ERROR_SUCCESS){
        wprintf(L"RASCREDENTIALS structure reset failed!\n");
        HeapFree(GetProcessHeap(), 0, lpCred);
        HeapFree(GetProcessHeap(), 0, lpentry);
        return 0;
    }

    // Grab the newly created entry's credentials
    dwRet = RasGetCredentials(NULL, lpszEntry, lpCred);
    if(dwRet == ERROR_SUCCESS){
        wprintf(L"The following credentials were retrieved for the entry: %s\n\tUser name: %s\n\tPassword: %s\n\tDomain: %s\n", lpszEntry, lpCred->szUserName, lpCred->szPassword, lpCred->szDomain);
    }else{
        wprintf(L"RasValidateEntryName failed: Error = %d\n", dwRet);
    }

    // Clean up: delete the new entry
    dwRet = RasDeleteEntry(NULL, lpszEntry);
    if (dwRet != ERROR_SUCCESS){
        wprintf(L"RasDeleteEntry failed: Error = %d\n", dwRet);
    }

    HeapFree(GetProcessHeap(), 0, lpentry);
    HeapFree(GetProcessHeap(), 0, lpCred);
    return 0;
}

```






> [!NOTE]
> The ras.h header defines RasGetCredentials as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)">RASCREDENTIALS</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetentrydialparamsa">RasGetEntryDialParams</a>



<a href="/windows/desktop/api/ras/nf-ras-rassetcredentialsa">RasSetCredentials</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
