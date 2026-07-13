---
UID: NF:rasdlg.RasEntryDlgA
title: RasEntryDlgA function (rasdlg.h)
description: The RasEntryDlg function displays modal property sheets that allow a user to manipulate phone-book entries. (ANSI)
helpviewer_keywords: ["RasEntryDlgA", "rasdlg/RasEntryDlgA"]
old-location: rras\rasentrydlg.htm
tech.root: RRAS
ms.assetid: 9259502d-c31b-4ebd-ace7-70f02bbb7873
ms.date: 12/05/2018
ms.keywords: RasEntryDlg, RasEntryDlg function [RAS], RasEntryDlgA, RasEntryDlgW, _ras_rasentrydlg, rasdlg/RasEntryDlg, rasdlg/RasEntryDlgA, rasdlg/RasEntryDlgW, rras.rasentrydlg
req.header: rasdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasEntryDlgW (Unicode) and RasEntryDlgA (ANSI)
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
 - RasEntryDlgA
 - rasdlg/RasEntryDlgA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasdlg.dll
api_name:
 - RasEntryDlg
 - RasEntryDlgA
 - RasEntryDlgW
---

# RasEntryDlgA function


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
<a href="/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)">RASENTRYDLG</a> structure.

<div class="alert"><b>Note</b>  The <b>RASEDFLAG_CloneEntry</b> flag has been deprecated, as of 
  Windows Vista and Windows Server 2008. It may be altered or unavailable in subsequent versions. Instead, copy an entry by calling <a href="/windows/desktop/api/ras/nf-ras-rasgetentrypropertiesa">RasGetEntryProperties</a> to get the entry and then calling <a href="/windows/desktop/api/ras/nf-ras-rassetentrypropertiesa">RasSetEntryProperties</a> to save the entry with a new name.</div>
<div> </div>
If you are creating an entry, this parameter is a default new entry name that the user can change. If this parameter is <b>NULL</b>, the function provides a default name. If you are creating an entry, set the <b>RASEDFLAG_NewEntry</b> flag in the <b>dwFlags</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)">RASENTRYDLG</a> structure.

### -param lpInfo [in]

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)">RASENTRYDLG</a> structure that specifies additional input and output parameters. The <b>dwSize</b> member of this structure must specify sizeof(<b>RASENTRYDLG</b>). Use the <b>dwFlags</b> member to indicate whether you are creating, editing, or copying an entry. If an error occurs, the <b>dwError</b> member returns an error code; otherwise, it returns zero.

## -returns

If the user creates, copies, or edits a phone-book entry, the return value is <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.

 If an error occurs, <b>RasEntryDlg</b> sets the <b>dwError</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)">RASENTRYDLG</a> structure to a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

## -remarks

The 
<a href="/windows/desktop/api/ras/nf-ras-rascreatephonebookentrya">RasCreatePhonebookEntry</a> and 
<a href="/windows/desktop/api/ras/nf-ras-raseditphonebookentrya">RasEditPhonebookEntry</a> functions call the 
<b>RasEntryDlg</b> function.

The following sample code brings up a property sheet to create a new entry. The <i>lpszEntry</i> variable specifies the default name for the new entry.


```cpp
#include <windows.h>
#include <stdio.h>
#include "ras.h"
#include "rasdlg.h"
#include <tchar.h>

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
    
    // The RASENTRYDLG->dwSize member has to be initialized or the RRAS APIs will fail below.
    lpEntry->dwSize = sizeof(RASENTRYDLG);
    lpEntry->dwFlags |= RASEDFLAG_NewEntry;

    // Create the new entry using a user dialog
    nRet = RasEntryDlg(NULL, lpszEntry, lpEntry);

    // Any error codes are returned in lpEntry
    dwRet = lpEntry->dwError;
    
    if (nRet == TRUE) {
        wprintf(L"New entry created: %s\n", lpEntry->szEntry);

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

```






> [!NOTE]
> The rasdlg.h header defines RASENTRYDLG as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)">RASENTRYDLG</a>



<a href="/windows/desktop/api/ras/nf-ras-rascreatephonebookentrya">RasCreatePhonebookEntry</a>



<a href="/windows/desktop/api/rasdlg/nc-rasdlg-rascustomentrydlgfn">RasCustomEntryDlg</a>



<a href="/windows/desktop/api/ras/nf-ras-raseditphonebookentrya">RasEditPhonebookEntry</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
