---
UID: NF:winuser.GetDlgItemTextW
title: GetDlgItemTextW function (winuser.h)
description: Retrieves the title or text associated with a control in a dialog box. (Unicode)
helpviewer_keywords: ["GetDlgItemText", "GetDlgItemText function [Dialog Boxes]", "GetDlgItemTextW", "_win32_GetDlgItemText", "_win32_getdlgitemtext_cpp", "dlgbox.getdlgitemtext", "winui._win32_getdlgitemtext", "winuser/GetDlgItemText", "winuser/GetDlgItemTextW"]
old-location: dlgbox\getdlgitemtext.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getdlgitemtext.htm
ms.date: 12/05/2018
ms.keywords: GetDlgItemText, GetDlgItemText function [Dialog Boxes], GetDlgItemTextA, GetDlgItemTextW, _win32_GetDlgItemText, _win32_getdlgitemtext_cpp, dlgbox.getdlgitemtext, winui._win32_getdlgitemtext, winuser/GetDlgItemText, winuser/GetDlgItemTextA, winuser/GetDlgItemTextW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDlgItemTextW (Unicode) and GetDlgItemTextA (ANSI)
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
 - GetDlgItemTextW
 - winuser/GetDlgItemTextW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-0.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - GetDlgItemText
 - GetDlgItemTextA
 - GetDlgItemTextW
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-0 (introduced in Windows 8)
---

# GetDlgItemTextW function


## -description

Retrieves the title or text associated with a control in a dialog box.

## -parameters

### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box that contains the control.

### -param nIDDlgItem [in]

Type: <b>int</b>

The identifier of the control whose title or text is to be retrieved.

### -param lpString [out]

Type: <b>LPTSTR</b>

The buffer to receive the title or text.

### -param cchMax [in]

Type: <b>int</b>

The maximum length, in characters, of the string to be copied to the buffer pointed to by <i>lpString</i>. If the length of the string, including the null character, exceeds the limit, the string is truncated.

## -returns

Type: <b>UINT</b>

If the function succeeds, the return value specifies the number of characters copied to the buffer, not including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the string is as long or longer than the buffer, the buffer will contain the truncated string with a terminating null character.

The <b>GetDlgItemText</b> function sends a <a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a> message to the control. 


#### Examples

For an example, see <a href="/windows/desktop/dlgbox/using-dialog-boxes">Creating a Modal Dialog Box</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines GetDlgItemText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint">GetDlgItemInt</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint">SetDlgItemInt</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta">SetDlgItemText</a>



<a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a>
