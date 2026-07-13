---
UID: NF:ras.RasEditPhonebookEntryA
title: RasEditPhonebookEntryA function (ras.h)
description: The RasEditPhonebookEntry function edits an existing phone-book entry. The function displays a dialog box in which the user can modify the existing information. (ANSI)
helpviewer_keywords: ["RasEditPhonebookEntryA", "ras/RasEditPhonebookEntryA"]
old-location: rras\raseditphonebookentry.htm
tech.root: RRAS
ms.assetid: 7fce1ea8-7ed6-4975-af4b-e20a1c1be5fa
ms.date: 12/05/2018
ms.keywords: RasEditPhonebookEntry, RasEditPhonebookEntry function [RAS], RasEditPhonebookEntryA, RasEditPhonebookEntryW, _ras_raseditphonebookentry, ras/RasEditPhonebookEntry, ras/RasEditPhonebookEntryA, ras/RasEditPhonebookEntryW, rras.raseditphonebookentry
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasEditPhonebookEntryW (Unicode) and RasEditPhonebookEntryA (ANSI)
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
 - RasEditPhonebookEntryA
 - ras/RasEditPhonebookEntryA
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
 - RasEditPhonebookEntry
 - RasEditPhonebookEntryA
 - RasEditPhonebookEntryW
---

# RasEditPhonebookEntryA function


## -description

<p class="CCE_Message">[This function has been deprecated as of Windows Vista and its functionality has been replaced by <a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasentrydlga">RasEntryDlg</a>.]

The 
<b>RasEditPhonebookEntry</b> function edits an existing phone-book entry. The function displays a dialog box in which the user can modify the existing information.

## -parameters

### -param unnamedParam1 [in]

Handle to the parent window of the dialog box.

### -param unnamedParam2 [in]

Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the<b> Dial-Up Networking</b> dialog box.

### -param unnamedParam3 [in]

Pointer to a null-terminated string that specifies the name of an existing entry in the phone-book file.

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
<dt><b>ERROR_BUFFER_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The phone-book entry buffer is invalid.

</td>
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

When calling <a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasentrydlga">RasEntryDlg</a>, set each member of the <a href="/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)">RASENTRYDLG</a> structure passed to <i>lpinfo</i> to zero except:

<ul>
<li><i>dwSize</i> = sizeof(<a href="/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)">RASENTRYDLG</a>)</li>
<li><i>hwndOwner</i>  = the <i>hwnd</i> parameter above</li>
</ul>




> [!NOTE]
> The ras.h header defines RasEditPhonebookEntry as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ras/nf-ras-rascreatephonebookentrya">RasCreatePhonebookEntry</a>



<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasentrydlga">RasEntryDlg</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetentrydialparamsa">RasGetEntryDialParams</a>



<a href="/windows/desktop/api/ras/nf-ras-rassetentrydialparamsa">RasSetEntryDialParams</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
