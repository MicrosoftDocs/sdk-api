---
UID: NF:winuser.SetDlgItemTextW
title: SetDlgItemTextW function (winuser.h)
description: Sets the title or text of a control in a dialog box. (Unicode)
helpviewer_keywords: ["SetDlgItemText", "SetDlgItemText function [Dialog Boxes]", "SetDlgItemTextW", "_win32_SetDlgItemText", "_win32_setdlgitemtext_cpp", "dlgbox.setdlgitemtext", "winui._win32_setdlgitemtext", "winuser/SetDlgItemText", "winuser/SetDlgItemTextW"]
old-location: dlgbox\setdlgitemtext.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\setdlgitemtext.htm
ms.date: 12/05/2018
ms.keywords: SetDlgItemText, SetDlgItemText function [Dialog Boxes], SetDlgItemTextA, SetDlgItemTextW, _win32_SetDlgItemText, _win32_setdlgitemtext_cpp, dlgbox.setdlgitemtext, winui._win32_setdlgitemtext, winuser/SetDlgItemText, winuser/SetDlgItemTextA, winuser/SetDlgItemTextW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetDlgItemTextW (Unicode) and SetDlgItemTextA (ANSI)
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
 - SetDlgItemTextW
 - winuser/SetDlgItemTextW
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
 - SetDlgItemText
 - SetDlgItemTextA
 - SetDlgItemTextW
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-0 (introduced in Windows 8)
---

# SetDlgItemTextW function


## -description

Sets the title or text of a control in a dialog box.

## -parameters

### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box that contains the control.

### -param nIDDlgItem [in]

Type: <b>int</b>

The control with a title or text to be set.

### -param lpString [in]

Type: <b>LPCTSTR</b>

The text to be copied to the control.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>SetDlgItemText</b> function sends a <a href="/windows/desktop/winmsg/wm-settext">WM_SETTEXT</a> message to the specified control. 


#### Examples

For an example, see <a href="/windows/desktop/Controls/using-list-boxes">Using List Boxes</a>. 

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines SetDlgItemText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint">GetDlgItemInt</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta">GetDlgItemText</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint">SetDlgItemInt</a>



<a href="/windows/desktop/winmsg/wm-settext">WM_SETTEXT</a>
