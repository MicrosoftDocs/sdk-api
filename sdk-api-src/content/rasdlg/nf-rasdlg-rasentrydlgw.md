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

# RasEntryDlgW function


## -description


The 
<b>RasEntryDlg</b> function displays modal property sheets that allow a user to manipulate phone-book entries. If editing or copying an existing phone-book entry, the function displays a phone-book entry property sheet. The 
<b>RasEntryDlg</b> function returns when the user closes the property sheet.


## -parameters




### -param lpszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.


### -param lpszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies the name of the phone-book entry to edit, copy, or create. 




If you are editing or copying an entry, this parameter is the name of an existing phone-book entry. If you are copying an entry, set the <b>RASEDFLAG_CloneEntry</b> flag in the <b>dwFlags</b> member of the 
<a href="https://msdn.microsoft.com/7a529aa6-3a75-44b8-bae3-0edc5c653825">RASENTRYDLG</a> structure.

<div class="alert"><b>Note</b>  The R<b>RASEDFLAG_CloneEntry</b> flag has been deprecated, as of 
  Windows Vista and Windows Server 2008. It may be altered or unavailable in subsequent versions. Instead, copy an entry by calling <a href="https://msdn.microsoft.com/eef9c197-04b3-4f3c-a7bd-8c62f9fac560">RasGetEntryProperties</a> to get the entry and then calling <a href="https://msdn.microsoft.com/6532b48b-0d80-4993-800e-c808bb7540d6">RasSetEntryProperties</a> to save the entry with a new name.</div>
<div> </div>
If you are creating an entry, this parameter is a default new entry name that the user can change. If this parameter is <b>NULL</b>, the function provides a default name. If you are creating an entry, set the <b>RASEDFLAG_NewEntry</b> flag in the <b>dwFlags</b> member of the 
<a href="https://msdn.microsoft.com/7a529aa6-3a75-44b8-bae3-0edc5c653825">RASENTRYDLG</a> structure.


### -param lpInfo [in]

Pointer to a 
<a href="https://msdn.microsoft.com/b7f3cd3f-3d16-407e-b17b-488ce2b00d43">RASENTRYDLG</a> structure that specifies additional input and output parameters. The <b>dwSize</b> member of this structure must specify sizeof(<b>RASENTRYDLG</b>). Use the <b>dwFlags</b> member to indicate whether you are creating, editing, or copying an entry. If an error occurs, the <b>dwError</b> member returns an error code; otherwise, it returns zero.


## -returns



If the user creates, copies, or edits a phone-book entry, the return value is <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.

 If an error occurs, <b>RasEntryDlg</b> sets the <b>dwError</b> member of the 
<a href="https://msdn.microsoft.com/b7f3cd3f-3d16-407e-b17b-488ce2b00d43">RASENTRYDLG</a> structure to a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.




## -remarks



The 
<a href="https://msdn.microsoft.com/da8bd49f-e890-4e8a-ab4d-7366c6f2b361">RasCreatePhonebookEntry</a> and 
<a href="https://msdn.microsoft.com/7fce1ea8-7ed6-4975-af4b-e20a1c1be5fa">RasEditPhonebookEntry</a> functions call the 
<b>RasEntryDlg</b> function.

The following sample code brings up a property sheet to create a new entry. The <i>lpszEntry</i> variable specifies the default name for the new entry.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include "ras.h"
#include "rasdlg.h"
#include &lt;tchar.h&gt;

DWORD __cdecl wmain(){

    DWORD dwRet = ERROR_SUCCESS;
    BOOL nRet = TRUE;
    LPTSTR lpszEntry = L"EntryName";

    // Allocate heap memory and initialize RASENTRYDLG structure
    LPRASENTRYDLG lpEntry = (LPRASENTRYDLG)HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, sizeof(RASENTRYDLG));
    if (lpEntry == NULL){
        wprintf(L"HeapAlloc failed.\n");
        return 0;
    }
    
    // The RASENTRYDLG-&gt;dwSize member has to be initialized or the RRAS APIs will fail below.
    lpEntry-&gt;dwSize = sizeof(RASENTRYDLG);
    lpEntry-&gt;dwFlags |= RASEDFLAG_NewEntry;

    // Create the new entry using a user dialog
    nRet = RasEntryDlg(NULL, lpszEntry, lpEntry);

    // Any error codes are returned in lpEntry
    dwRet = lpEntry-&gt;dwError;
    
    if (nRet == TRUE) {
        wprintf(L"New entry created: %s\n", lpEntry-&gt;szEntry);

        // Clean up: delete the new entry
        dwRet = RasDeleteEntry(NULL, lpszEntry);
        if (dwRet != ERROR_SUCCESS) {
            wprintf(L"RasDeleteEntry failed: Error = %d\n", dwRet);
        }

    } 
    else {
        if (dwRet != ERROR_SUCCESS) {
            wprintf(L"RasEntryDlg failed: Error = %d\n", dwRet);
        }
        else {
            wprintf(L"User pressed Cancel\n");
        }
    }

    HeapFree(GetProcessHeap(), 0, lpEntry);
    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b7f3cd3f-3d16-407e-b17b-488ce2b00d43">RASENTRYDLG</a>



<a href="https://msdn.microsoft.com/da8bd49f-e890-4e8a-ab4d-7366c6f2b361">RasCreatePhonebookEntry</a>



<a href="https://msdn.microsoft.com/4778069b-87d0-4379-95f7-718fe0d7a56c">RasCustomEntryDlg</a>



<a href="https://msdn.microsoft.com/7fce1ea8-7ed6-4975-af4b-e20a1c1be5fa">RasEditPhonebookEntry</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

