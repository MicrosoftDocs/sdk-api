---
UID: NF:ras.RasDeleteEntryA
title: RasDeleteEntryA function
author: windows-sdk-content
description: The RasDeleteEntry function deletes an entry from a phone book.
old-location: rras\rasdeleteentry.htm
old-project: rras
ms.assetid: 80a6c2d3-917b-4d13-867f-a1399d434105
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RasDeleteEntry, RasDeleteEntry function [RAS], RasDeleteEntryA, RasDeleteEntryW, _ras_rasdeleteentry, ras/RasDeleteEntry, ras/RasDeleteEntryA, ras/RasDeleteEntryW, rras.rasdeleteentry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: RASPROJECTION_INFO_TYPE
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
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: ADAM
---

# RasDeleteEntryA function


## -description


The 
<b>RasDeleteEntry</b> function deletes an entry from a phone book.


## -parameters




### -param

TBD




#### - [in]

 Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box. 




<b>Windows Me/98/95:  </b>This parameter should always be <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.


#### - lpszEntry [in]

Pointer to a null-terminated string that specifies the name of an existing entry to be deleted.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;stdio.h&gt;
#include &lt;windows.h&gt;
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
  
    // The RASENTRY-&gt;dwSize member has to be initialized or the RRAS APIs will fail below.
    lpentry-&gt;dwSize = sizeof(RASENTRY);
    lpentry-&gt;dwFramingProtocol = RASFP_Ppp;
    lpentry-&gt;dwfOptions = 0;
    lpentry-&gt;dwType = RASET_Phone;
    dwRet |= StringCchCopyN(lpentry-&gt;szLocalPhoneNumber, RAS_MaxPhoneNumber, lpszphonenumber, PHONE_NUMBER_LENGTH);
    dwRet |= StringCchCopyN(lpentry-&gt;szDeviceName, RAS_MaxDeviceName, lpszdevicename, DEVICE_NAME_LENGTH);
    dwRet |= StringCchCopyN(lpentry-&gt;szDeviceType, RAS_MaxDeviceType, lpszdevicetype, DEVICE_TYPE_LENGTH);
    if (dwRet != ERROR_SUCCESS){
        wprintf(L"RASENTRY structure initilization failed");
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
    dwRet = RasSetEntryProperties(NULL, lpszEntry, lpentry, lpentry-&gt;dwSize, NULL, 0);
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/da8bd49f-e890-4e8a-ab4d-7366c6f2b361">RasCreatePhonebookEntry</a>



<a href="https://msdn.microsoft.com/9df7402f-c93e-45d4-925a-f2ce9d547bce">RasEnumEntries</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

