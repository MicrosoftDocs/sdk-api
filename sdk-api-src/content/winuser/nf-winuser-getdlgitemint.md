---
UID: NF:winuser.GetDlgItemInt
title: GetDlgItemInt function (winuser.h)
description: Translates the text of a specified control in a dialog box into an integer value.
helpviewer_keywords: ["GetDlgItemInt","GetDlgItemInt function [Dialog Boxes]","_win32_GetDlgItemInt","_win32_getdlgitemint_cpp","dlgbox.getdlgitemint","winui._win32_getdlgitemint","winuser/GetDlgItemInt"]
old-location: dlgbox\getdlgitemint.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getdlgitemint.htm
ms.date: 12/05/2018
ms.keywords: GetDlgItemInt, GetDlgItemInt function [Dialog Boxes], _win32_GetDlgItemInt, _win32_getdlgitemint_cpp, dlgbox.getdlgitemint, winui._win32_getdlgitemint, winuser/GetDlgItemInt
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDlgItemInt
 - winuser/GetDlgItemInt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - GetDlgItemInt
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# GetDlgItemInt function


## -description

Translates the text of a specified control in a dialog box into an integer value.

## -parameters

### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box that contains the control of interest.

### -param nIDDlgItem [in]

Type: <b>int</b>

The identifier of the control whose text is to be translated.

### -param lpTranslated [out, optional]

Type: <b>BOOL*</b>

Indicates success or failure (<b>TRUE</b> indicates success, <b>FALSE</b> indicates failure). 

If this parameter is <b>NULL</b>, the function returns no information about success or failure.

### -param bSigned [in]

Type: <b>BOOL</b>

Indicates whether the function should examine the text for a minus sign at the beginning and return a signed integer value if it finds one (<b>TRUE</b> specifies this should be done, <b>FALSE</b> that it should not).

## -returns

Type: <b>UINT</b>

If the function succeeds, the variable pointed to by <i>lpTranslated</i> is set to <b>TRUE</b>, and the return value is the translated value of the control text. 

If the function fails, the variable pointed to by <i>lpTranslated</i> is set to <b>FALSE</b>, and the return value is zero. Note that, because zero is a possible translated value, a return value of zero does not by itself indicate failure.

If <i>lpTranslated</i> is <b>NULL</b>, the function returns no information about success or failure.

Note that, if the <i>bSigned</i> parameter is <b>TRUE</b> and there is a minus sign (–) at the beginning of the text, <b>GetDlgItemInt</b> translates the text into a signed integer value. Otherwise, the function creates an unsigned integer value. To obtain the proper value in this case, cast the return value to an <b>int</b> type.

To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>GetDlgItemInt</b> function retrieves the text of the specified control by sending the control a <a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a> message. The function translates the retrieved text by stripping any extra spaces at the beginning of the text and then converting the decimal digits. The function stops translating when it reaches the end of the text or encounters a nonnumeric character. 

The <b>GetDlgItemInt</b> function returns zero if the translated value is greater than <b>INT_MAX</b> (for signed numbers) or <b>UINT_MAX</b> (for unsigned numbers). 


#### Examples

For an example, see <a href="/windows/desktop/dlgbox/using-dialog-boxes">Creating a Modeless Dialog Box</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdlgctrlid">GetDlgCtrlID</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdlgitem">GetDlgItem</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta">GetDlgItemText</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint">SetDlgItemInt</a>
