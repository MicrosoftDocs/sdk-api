---
UID: NF:ras.RasCreatePhonebookEntryW
title: RasCreatePhonebookEntryW function (ras.h)
description: The RasCreatePhonebookEntry function creates a new phone-book entry. The function displays a dialog box in which the user types information for the phone-book entry. (Unicode)
helpviewer_keywords: ["RasCreatePhonebookEntry", "RasCreatePhonebookEntry function [RAS]", "RasCreatePhonebookEntryW", "_ras_rascreatephonebookentry", "ras/RasCreatePhonebookEntry", "ras/RasCreatePhonebookEntryW", "rras.rascreatephonebookentry"]
old-location: rras\rascreatephonebookentry.htm
tech.root: RRAS
ms.assetid: da8bd49f-e890-4e8a-ab4d-7366c6f2b361
ms.date: 12/05/2018
ms.keywords: RasCreatePhonebookEntry, RasCreatePhonebookEntry function [RAS], RasCreatePhonebookEntryA, RasCreatePhonebookEntryW, _ras_rascreatephonebookentry, ras/RasCreatePhonebookEntry, ras/RasCreatePhonebookEntryA, ras/RasCreatePhonebookEntryW, rras.rascreatephonebookentry
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasCreatePhonebookEntryW
 - ras/RasCreatePhonebookEntryW
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
 - RasCreatePhonebookEntry
 - RasCreatePhonebookEntryA
 - RasCreatePhonebookEntryW
---

# RasCreatePhonebookEntryW function


## -description

<p class="CCE_Message">[This function has been deprecated as of Windows Vista and its functionality has been replaced by <a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga">RasDialDlg</a>. ]

The 
<b>RasCreatePhonebookEntry</b> function creates a new phone-book entry. The function displays a dialog box in which the user types information for the phone-book entry.

## -parameters

### -param unnamedParam1 [in]

Handle to the parent window of the dialog box.

### -param unnamedParam2 [in]

 Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

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

When calling <a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga">RasDialDlg</a>, set each member of the <b>RASDIALDLG</b> structure passed to <i>lpInfo</i> to zero except:

<ul>
<li><i>dwSize</i> = sizeof(<b>RASDIALDLG</b>)</li>
<li><i>hwndOwner</i>  = the <i>hwnd</i> parameter above</li>
<li><i>dwFlags</i> = <b>RASEDFLAG_NewEntry</b></li>
</ul>




> [!NOTE]
> The ras.h header defines RasCreatePhonebookEntry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ras/nf-ras-raseditphonebookentrya">RasEditPhonebookEntry</a>



<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasentrydlga">RasEntryDlg</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetentrydialparamsa">RasGetEntryDialParams</a>



<a href="/windows/desktop/api/ras/nf-ras-rassetentrydialparamsa">RasSetEntryDialParams</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
