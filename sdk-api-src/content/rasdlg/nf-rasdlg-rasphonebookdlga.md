---
UID: NF:rasdlg.RasPhonebookDlgA
title: RasPhonebookDlgA function
author: windows-sdk-content
description: The RasPhonebookDlg function displays the main Dial-Up Networking dialog box.
old-location: rras\rasphonebookdlg.htm
tech.root: rras
ms.assetid: 64603090-ec03-4eac-9da6-cb631c97dfb5
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: RasPhonebookDlg, RasPhonebookDlg function [RAS], RasPhonebookDlgA, RasPhonebookDlgW, _ras_rasphonebookdlg, rasdlg/RasPhonebookDlg, rasdlg/RasPhonebookDlgA, rasdlg/RasPhonebookDlgW, rras.rasphonebookdlg
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rasdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasPhonebookDlgW (Unicode) and RasPhonebookDlgA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasdlg.lib
req.dll: Rasdlg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasdlg.dll
api_name:
 - RasPhonebookDlg
 - RasPhonebookDlgA
 - RasPhonebookDlgW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasPhonebookDlgA function


## -description


The 
<b>RasPhonebookDlg</b> function displays the main <b>Dial-Up Networking</b> dialog box. From this modal dialog box, the user can dial, edit, or delete a selected phone-book entry, create a new phone-book entry, or specify user preferences. The 
<b>RasPhonebookDlg</b> function returns when the dialog box closes.


## -parameters




### -param lpszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.


### -param lpszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies the name of the phone-book entry to highlight initially. If this parameter is <b>NULL</b>, or if the specified entry does not exist, the dialog box highlights the first entry in the alphabetic list.


### -param lpInfo [in, out]

Pointer to the 
<a href="https://msdn.microsoft.com/fa5843ec-1f39-40b2-8c5a-9b72f3cc3539">RASPBDLG</a> structure that specifies additional input and output parameters. 




On input, the <b>dwSize</b> member of this structure must specify the sizeof(
<a href="https://msdn.microsoft.com/fa5843ec-1f39-40b2-8c5a-9b72f3cc3539">RASPBDLG</a>).

If an error occurs, the <b>dwError</b> member of the structure receives, on output, an error code; otherwise, it receives zero.


## -returns



If the user selects the <b>Connect</b> button and the function establishes a connection, the return value is <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.

 If an error occurs, the <b>dwError</b> member of the 
<a href="https://msdn.microsoft.com/fa5843ec-1f39-40b2-8c5a-9b72f3cc3539">RASPBDLG</a> structure returns a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

The following sample code brings up the <b>Dial-Up Networking</b> dialog. The dialog  displays dialing information for the first entry from the default phonebook file.

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
#pragma comment(lib, "rasapi32.lib")

int main (){
    
    // Initialize the return code
    BOOL nRet = TRUE;

    // Allocate heap memory for the RASPBLDG structure
    RASPBDLG * lpInfo = (LPRASPBDLG)HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY, sizeof(RASPBDLG));
    
    // The dwsize member of lpInfo must contain the structure size, or the 
    // call to RasPhonebookDlg will fail
    lpInfo-&gt;dwSize = sizeof(RASPBDLG);
     
    // Open a user dialog box  
    nRet = RasPhonebookDlg(NULL,NULL,lpInfo);
    
    if(nRet == TRUE){
        // The user dialed a connection successfully
        printf("User pressed Connect\n");
    }else{
        if(lpInfo-&gt;dwError != 0){
            printf("RasPhonebookDlg failed: Error = %d\n", lpInfo-&gt;dwError);
        }else{
            // The user closed the dialog box manually
            printf("User pressed Close\n");
        }
    }

    // Free the heap memory for the RASPBLDG structure
    HeapFree(GetProcessHeap(), 0, lpInfo);
    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fa5843ec-1f39-40b2-8c5a-9b72f3cc3539">RASPBDLG</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

