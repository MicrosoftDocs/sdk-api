---
UID: NF:ras.RasEnumEntriesW
title: RasEnumEntriesW function
author: windows-sdk-content
description: The RasEnumEntries function lists all entry names in a remote access phone book.
old-location: rras\rasenumentries.htm
old-project: rras
ms.assetid: 9df7402f-c93e-45d4-925a-f2ce9d547bce
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: RasEnumEntries, RasEnumEntries function [RAS], RasEnumEntriesA, RasEnumEntriesW, _ras_rasenumentries, ras/RasEnumEntries, ras/RasEnumEntriesA, ras/RasEnumEntriesW, rras.rasenumentries
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
req.unicode-ansi: RasEnumEntriesW (Unicode) and RasEnumEntriesA (ANSI)
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
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasEnumEntries
 - RasEnumEntriesA
 - RasEnumEntriesW
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: ADAM
---

# RasEnumEntriesW function


## -description


The 
<b>RasEnumEntries</b> function lists all entry names in a remote access phone book.


## -parameters




### -param

TBD




#### - lpcEntries [out]

Pointer to a variable that receives to the number of phone-book entries written to the buffer specified by <i>lprasentryname</i>.


#### - lpcb [in, out]

Pointer to a variable that, on input, contains the size, in bytes, of the buffer specified by <i>lprasentryname</i>. 




Pointer to a variable that, on output, contains the size, in bytes, of the array of 
<a href="https://msdn.microsoft.com/3761d4cd-b573-44b6-b617-c8dd45b479ea">RASENTRYNAME</a> structures required for the phone-book entries.

<b>Windows Vista or later:  </b>To determine the required buffer size, call 
<b>RasEnumEntries</b> with <i>lprasentryname</i> set to <b>NULL</b>. The variable pointed to by <i>lpcb</i> should be set to zero. The function will return the required buffer size in <i>lpcb</i> and an error code of <b>ERROR_BUFFER_TOO_SMALL</b>.


#### - lprasentryname [in, out]

Pointer to a buffer that, on output, receives an array of 
<a href="https://msdn.microsoft.com/3761d4cd-b573-44b6-b617-c8dd45b479ea">RASENTRYNAME</a> structures, one for each phone-book entry. 




On input, an application must set the <b>dwSize</b> member of the first 
<a href="https://msdn.microsoft.com/3761d4cd-b573-44b6-b617-c8dd45b479ea">RASENTRYNAME</a> structure in the buffer to sizeof(<b>RASENTRYNAME</b>) in order to identify the version of the structure being passed.


#### - lpszPhonebook [in]

Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.

If this parameter is <b>NULL</b>, the entries are enumerated from all the remote access phone-book files in the AllUsers profile and the user's profile.


#### - reserved [in]

Reserved; must be <b>NULL</b>.


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
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>lprasentryname</i> buffer is not large enough. The <i>lpcb</i>
								 parameter is less than the <b>dwSize</b> member in the <i>lprasentryname</i>
								 parameter which should be set prior to calling the function. The function returns the required buffer size in the variable pointed to by <i>lpcb</i>.

<b>Windows Vista or later:  </b>The <i>lprasentryname</i> buffer may be set to <b>NULL</b> and the variable pointed to by <i>lpcb</i> may be set to zero. The function will return the required buffer size in the variable pointed to by <i>lpcb</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The value of <b>dwSize</b> in the 
<a href="https://msdn.microsoft.com/3761d4cd-b573-44b6-b617-c8dd45b479ea">RASENTRYNAME</a> structure pointed to by <i>lprasentryname</i>, specifies a version of the structure that is not supported on the current platform. For example, on Windows 95, 
<b>RasEnumEntries</b> returns this error if <b>dwSize</b> indicates that 
<a href="https://msdn.microsoft.com/3761d4cd-b573-44b6-b617-c8dd45b479ea">RASENTRYNAME</a> includes the <b>dwFlags</b> and <b>szPhonebookPath</b> members, since these members are not supported on Windows 95 (they are supported only on Windows 2000 and later).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate sufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



The following sample code enumerates the RAS phone-book entries on Windows Vista and later versions of Windows. The code initially calls 
<b>RasEnumEntries</b> to obtain the size of the buffer to pass in. The code then calls 
<b>RasEnumEntries</b> again, to enumerate the entries. Note that for the second call, the code sets the <b>dwSize</b> member of the first 
<a href="https://msdn.microsoft.com/3761d4cd-b573-44b6-b617-c8dd45b479ea">RASENTRYNAME</a> structure in the buffer to sizeof(<b>RASENTRYNAME</b>) to specify the structure version.

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
    DWORD dwEntries = 0;
    LPRASENTRYNAME lpRasEntryName = NULL;
    
    // Call RasEnumEntries with lpRasEntryName = NULL. dwCb is returned with the required buffer size and 
    // a return code of ERROR_BUFFER_TOO_SMALL
    dwRet = RasEnumEntries(NULL, NULL, lpRasEntryName, &amp;dwCb, &amp;dwEntries);

    if (dwRet == ERROR_BUFFER_TOO_SMALL){
        // Allocate the memory needed for the array of RAS entry names.
        lpRasEntryName = (LPRASENTRYNAME) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, dwCb);
        if (lpRasEntryName == NULL){
            wprintf(L"HeapAlloc failed!\n");
            return 0;
        }
        // The first RASENTRYNAME structure in the array must contain the structure size
        lpRasEntryName[0].dwSize = sizeof(RASENTRYNAME);
        
        // Call RasEnumEntries to enumerate all RAS entry names
        dwRet = RasEnumEntries(NULL, NULL, lpRasEntryName, &amp;dwCb, &amp;dwEntries);

        // If successful, print the RAS entry names 
        if (ERROR_SUCCESS == dwRet){
            wprintf(L"The following RAS entry names were found:\n");
            for (DWORD i = 0; i &lt; dwEntries; i++){
                wprintf(L"%s\n", lpRasEntryName[i].szEntryName);
            }
        }
        //Deallocate memory for the connection buffer
        HeapFree(GetProcessHeap(), 0, lpRasEntryName);
        lpRasEntryName = NULL;
        return 0;
    }

    // There was either a problem with RAS or there are RAS entry names to enumerate    
    if(dwEntries &gt;= 1){
        wprintf(L"The operation failed to acquire the buffer size.\n");
    }else{
        wprintf(L"There were no RAS entry names found:.\n");
    }

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3761d4cd-b573-44b6-b617-c8dd45b479ea">RASENTRYNAME</a>



<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

