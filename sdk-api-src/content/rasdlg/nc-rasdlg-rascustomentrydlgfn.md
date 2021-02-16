---
UID: NC:rasdlg.RasCustomEntryDlgFn
title: RasCustomEntryDlgFn (rasdlg.h)
description: The RasCustomEntryDlg function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom dialogs for managing phone-book entries.
helpviewer_keywords: ["RasCustomEntryDlg","RasCustomEntryDlg callback function [RAS]","RasCustomEntryDlgFn","RasCustomEntryDlgFn callback","_ras_rascustomentrydlg","rasdlg/RasCustomEntryDlg","rras.rascustomentrydlg"]
old-location: rras\rascustomentrydlg.htm
tech.root: RRAS
ms.assetid: 4778069b-87d0-4379-95f7-718fe0d7a56c
ms.date: 12/05/2018
ms.keywords: RasCustomEntryDlg, RasCustomEntryDlg callback function [RAS], RasCustomEntryDlgFn, RasCustomEntryDlgFn callback, _ras_rascustomentrydlg, rasdlg/RasCustomEntryDlg, rras.rascustomentrydlg
req.header: rasdlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasCustomEntryDlgFn
 - rasdlg/RasCustomEntryDlgFn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Rasdlg.h
api_name:
 - RasCustomEntryDlg
---

# RasCustomEntryDlgFn callback function


## -description

The 
<b>RasCustomEntryDlg</b> function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom dialogs for managing phone-book entries.

## -parameters

### -param hInstDll

Handle to the instance of the custom-dial DLL that was loaded.

### -param lpszPhonebook

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box.

### -param lpszEntry

Pointer to a <b>null</b>-terminated string that contains the name of the phone-book entry to edit, copy, or create. 




If you are editing or copying an entry, this parameter is the name of an existing phone-book entry. If you are copying an entry, set the RASEDFLAG_CloneEntry flag in the <b>dwFlags</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)">RASENTRYDLG</a> structure.

If you are creating an entry, this parameter is a default new entry name that the user can change. If this parameter is <b>NULL</b>, the function provides a default name. If you are creating an entry, set the RASEDFLAG_NewEntry flag in the <b>dwFlags</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)">RASENTRYDLG</a> structure.

### -param lpInfo

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)">RASENTRYDLG</a> structure that contains additional input and output parameters. On input, the <b>dwSize</b> member of this structure must specify sizeof(
<b>RASENTRYDLG</b>). Use the <b>dwSize</b> member to indicate whether creating, editing, or copying an entry. If an error occurs, the <b>dwError</b> member returns an error code; otherwise, it returns zero.

### -param dwFlags

Reserved for future use.

## -returns

If the user creates, copies, or edits a phone-book entry, the return value should be <b>TRUE</b>. Otherwise, the function should return <b>FALSE</b>.

If an error occurs, <b>RasCustomEntryDlg</b> should set the <b>dwError</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)">RASENTRYDLG</a> structure to a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

## -remarks

RAS  calls this entry point from 
<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasentrydlga">RasEntryDlg</a>, if the <b>szCustomDialDll</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a> structure for the entry being dialed specifies a custom-dialing DLL.

If the custom-dial DLL does not support this entry point, RAS returns ERROR_NO_CUSTOMENTRYDLG to the caller of 
<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasentrydlga">RasEntryDlg</a>.

## -see-also

<a href="/windows/desktop/RRAS/custom-dialers">Custom Dialers</a>



<a href="/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)">RASENTRY</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomdialfn">RasCustomDial</a>



<a href="/windows/desktop/api/rasdlg/nc-rasdlg-rascustomdialdlgfn">RasCustomDialDlg</a>



<a href="/windows/desktop/api/ras/nc-ras-rascustomhangupfn">RasCustomHangUp</a>



<a href="/windows/desktop/api/rasdlg/nf-rasdlg-rasentrydlga">RasEntryDlg</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>