---
UID: NF:ras.RasCreatePhonebookEntryW
title: RasCreatePhonebookEntryW function
author: windows-sdk-content
description: The RasCreatePhonebookEntry function creates a new phone-book entry. The function displays a dialog box in which the user types information for the phone-book entry.
old-location: rras\rascreatephonebookentry.htm
tech.root: rras
ms.assetid: da8bd49f-e890-4e8a-ab4d-7366c6f2b361
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: RasCreatePhonebookEntry, RasCreatePhonebookEntry function [RAS], RasCreatePhonebookEntryA, RasCreatePhonebookEntryW, _ras_rascreatephonebookentry, ras/RasCreatePhonebookEntry, ras/RasCreatePhonebookEntryA, ras/RasCreatePhonebookEntryW, rras.rascreatephonebookentry
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
req.unicode-ansi: RasCreatePhonebookEntryW (Unicode) and RasCreatePhonebookEntryA (ANSI)
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
 - RasCreatePhonebookEntry
 - RasCreatePhonebookEntryA
 - RasCreatePhonebookEntryW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RasCreatePhonebookEntryW
: 
---

# RasCreatePhonebookEntryW function


## -description


<p class="CCE_Message">[This function has been deprecated as of Windows Vista and its functionality has been replaced by <a href="https://msdn.microsoft.com/698a18a1-b302-4b0d-8399-0bbdbe775f08">RasDialDlg</a>. ]

The 
<b>RasCreatePhonebookEntry</b> function creates a new phone-book entry. The function displays a dialog box in which the user types information for the phone-book entry.


## -parameters




### -param arg1 [in]

Handle to the parent window of the dialog box.


### -param arg2 [in]

 Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box. 



					


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
The phone book is corrupted or missing components.

</td>
</tr>
</table>
 




## -remarks



When calling <a href="https://msdn.microsoft.com/698a18a1-b302-4b0d-8399-0bbdbe775f08">RasDialDlg</a>, set each member of the <b>RASDIALDLG</b> structure passed to <i>lpInfo</i> to zero except:

<ul>
<li><i>dwSize</i> = sizeof(<b>RASDIALDLG</b>)</li>
<li><i>hwndOwner</i>  = the <i>hwnd</i> parameter above</li>
<li><i>dwFlags</i> = <b>RASEDFLAG_NewEntry</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/7fce1ea8-7ed6-4975-af4b-e20a1c1be5fa">RasEditPhonebookEntry</a>



<a href="https://msdn.microsoft.com/9259502d-c31b-4ebd-ace7-70f02bbb7873">RasEntryDlg</a>



<a href="https://msdn.microsoft.com/c6752f95-c7e8-44d9-9dbd-9f03cc4778fa">RasGetEntryDialParams</a>



<a href="https://msdn.microsoft.com/e1acd68e-796e-49a2-8c7d-c0fd1a9764ef">RasSetEntryDialParams</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

