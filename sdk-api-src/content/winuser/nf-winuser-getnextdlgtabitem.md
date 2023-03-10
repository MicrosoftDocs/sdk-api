---
UID: NF:winuser.GetNextDlgTabItem
title: GetNextDlgTabItem function (winuser.h)
description: Retrieves a handle to the first control that has the WS_TABSTOP style that precedes (or follows) the specified control.
helpviewer_keywords: ["GetNextDlgTabItem","GetNextDlgTabItem function [Dialog Boxes]","_win32_GetNextDlgTabItem","_win32_getnextdlgtabitem_cpp","dlgbox.getnextdlgtabitem","winui._win32_getnextdlgtabitem","winuser/GetNextDlgTabItem"]
old-location: dlgbox\getnextdlgtabitem.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getnextdlgtabitem.htm
ms.date: 12/05/2018
ms.keywords: GetNextDlgTabItem, GetNextDlgTabItem function [Dialog Boxes], _win32_GetNextDlgTabItem, _win32_getnextdlgtabitem_cpp, dlgbox.getnextdlgtabitem, winui._win32_getnextdlgtabitem, winuser/GetNextDlgTabItem
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
 - GetNextDlgTabItem
 - winuser/GetNextDlgTabItem
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
 - GetNextDlgTabItem
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# GetNextDlgTabItem function


## -description

Retrieves a handle to the first 
		control that has the <a href="/windows/desktop/dlgbox/dlgbox-programming-considerations">WS_TABSTOP</a> 
		style that precedes (or follows) the specified control.

## -parameters

### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box to be searched.

### -param hCtl [in, optional]

Type: <b>HWND</b>

A handle to the control to be used as the starting point for the search. 
				If this parameter is <b>NULL</b>, the function fails.

### -param bPrevious [in]

Type: <b>BOOL</b>

Indicates how the function is to search the dialog box. If this parameter 
				is <b>TRUE</b>, the function searches for the previous control 
				in the dialog box. If this parameter is <b>FALSE</b>, the function searches 
				for the next control in the dialog box.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is the window handle 
				of the previous (or next) control that has the 
				<a href="/windows/desktop/dlgbox/dlgbox-programming-considerations">WS_TABSTOP</a> style set. 

If the function fails, the return value is <b>NULL</b>. To get extended error 
				information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>GetNextDlgTabItem</b> function searches controls in the order (or reverse order) they were created in the dialog box template. The function returns the first control it locates that is visible, not disabled, and has the <a href="/windows/desktop/dlgbox/dlgbox-programming-considerations">WS_TABSTOP</a> style. If no such control exists, the function returns <i>hCtl</i>. 

If the search for the next control with the <b>WS_TABSTOP</b> style encounters a window with the <b>WS_EX_CONTROLPARENT</b> style, the system recursively searches the window's children.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdlgitem">GetDlgItem</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getnextdlggroupitem">GetNextDlgGroupItem</a>



<b>Reference</b>
