---
UID: NF:ras.RasRenameEntryA
title: RasRenameEntryA function
author: windows-sdk-content
description: The RasRenameEntry function changes the name of an entry in a phone book.
old-location: rras\rasrenameentry.htm
tech.root: RRAS
ms.assetid: 95c63e58-c96d-43ad-8878-ba9e29f53f6e
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RasRenameEntry, RasRenameEntry function [RAS], RasRenameEntryA, RasRenameEntryW, _ras_rasrenameentry, ras/RasRenameEntry, ras/RasRenameEntryA, ras/RasRenameEntryW, rras.rasrenameentry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasRenameEntryW (Unicode) and RasRenameEntryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasRenameEntry
 - RasRenameEntryA
 - RasRenameEntryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasRenameEntryA function


## -description


The 
<b>RasRenameEntry</b> function changes the name of an entry in a phone book.


## -parameters




### -param arg1 [in]

Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.
						

<b>Windows Me/98/95:  </b>This parameter should always be <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.


### -param arg2 [in]

Pointer to a null-terminated string that specifies an existing entry name.


### -param arg3 [in]

Pointer to a null-terminated string that specifies the new entry name. Before calling 
<b>RasRenameEntry</b>, call the 
<a href="https://msdn.microsoft.com/c70ad0d4-6bc1-4716-9a8e-0fbeb55b7560">RasValidateEntryName</a> function to validate the new entry name.


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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate sufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpszNewEntry</i> name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
An entry with the <i>lpszNewEntry</i> name already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
The phone-book entry does not exist.

</td>
</tr>
</table>
 




## -remarks



The 
<b>RasRenameEntry</b> function allows entry names that would not be accepted by the dial-up networking user interface. The entry names specified in 
<b>RasRenameEntry</b> can consist of any string that adheres to the following conditions:

<ol>
<li>The string cannot have a length greater than RAS_MaxEntryName (as defined in Ras.h).</li>
<li>The string cannot consist entirely of space or tab characters.</li>
<li>The first character in the string cannot be a period character (".").</li>
</ol>
The following code sample renames the phone-book entry with the name specified by <i>pszOldName</i> to the new name specified by <i>pszNewName</i>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include "ras.h"
#include &lt;tchar.h&gt;

DWORD main (){

    DWORD dwErr = ERROR_SUCCESS;
    LPCTSTR pszOldName = L"RAS Connection 1\0";
    LPCTSTR pszNewName = L"RAS Connection 2\0";

    dwErr = RasValidateEntryName(NULL, pszNewName);
    if (ERROR_SUCCESS != dwErr)
    {
        printf("RasValidateEntryName failed: Error = %d\n", dwErr);
        return dwErr;
    }

    dwErr = RasRenameEntry(NULL, pszOldName, pszNewName);
    if (ERROR_SUCCESS != dwErr)
    {
        printf("RasRenameEntry failed: Error = %d\n", dwErr);
        return dwErr;
    }

    printf("Successfully renamed entry '%s' to '%s'\n", pszOldName, pszNewName);

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c70ad0d4-6bc1-4716-9a8e-0fbeb55b7560">RasValidateEntryName</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

