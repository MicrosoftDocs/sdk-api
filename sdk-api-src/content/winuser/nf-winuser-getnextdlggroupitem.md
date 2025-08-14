---
UID: NF:winuser.GetNextDlgGroupItem
title: GetNextDlgGroupItem function (winuser.h)
description: Retrieves a handle to the first control in a group of controls that precedes (or follows) the specified control in a dialog box.
helpviewer_keywords: ["GetNextDlgGroupItem","GetNextDlgGroupItem function [Dialog Boxes]","_win32_GetNextDlgGroupItem","_win32_getnextdlggroupitem_cpp","dlgbox.getnextdlggroupitem","winui._win32_getnextdlggroupitem","winuser/GetNextDlgGroupItem"]
old-location: dlgbox\getnextdlggroupitem.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getnextdlggroupitem.htm
ms.date: 12/05/2018
ms.keywords: GetNextDlgGroupItem, GetNextDlgGroupItem function [Dialog Boxes], _win32_GetNextDlgGroupItem, _win32_getnextdlggroupitem_cpp, dlgbox.getnextdlggroupitem, winui._win32_getnextdlggroupitem, winuser/GetNextDlgGroupItem
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
 - GetNextDlgGroupItem
 - winuser/GetNextDlgGroupItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-0.dll
 - User32.dll
api_name:
 - GetNextDlgGroupItem
---

# GetNextDlgGroupItem function


## -description

Retrieves a handle to the first control in a group of controls that precedes (or follows) the specified control in a dialog box.

## -parameters

### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box to be searched.

### -param hCtl [in, optional]

Type: <b>HWND</b>

A handle to the control to be used as the starting point for the search. If this parameter is <b>NULL</b>, the function uses the last (or first) control in the dialog box as the starting point for the search.

### -param bPrevious [in]

Type: <b>BOOL</b>

Indicates how the function is to search the group of controls in the dialog box. If this parameter is <b>TRUE</b>, the function searches for the previous control in the group. If it is <b>FALSE</b>, the function searches for the next control in the group.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is a handle to the previous (or next) control in the group of controls. 

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>GetNextDlgGroupItem</b> function searches controls in the order (or reverse order) they were created in the dialog box template. The first control in the group must have the <a href="/windows/desktop/dlgbox/dlgbox-programming-considerations">WS_GROUP</a> style; all other controls in the group must have been consecutively created and must not have the <b>WS_GROUP</b> style. 

When searching for the previous control, the function returns the first control it locates that is visible and not disabled. If the control specified by <i>hCtl</i> has the <b>WS_GROUP</b> style, the function temporarily reverses the search to locate the first control having the <b>WS_GROUP</b> style, then resumes the search in the original direction, returning the first control it locates that is visible and not disabled, or returning <i>hCtl</i> if no such control is found. 

When searching for the next control, the function returns the first control it locates that is visible, not disabled, and does not have the <b>WS_GROUP</b> style. If it encounters a control having the <b>WS_GROUP</b> style, the function reverses the search, locates the first control having the <b>WS_GROUP</b> style, and returns this control if it is visible and not disabled. Otherwise, the function resumes the search in the original direction and returns the first control it locates that is visible and not disabled, or returns <i>hCtl</i> if no such control is found. 

If the search for the next control in the group encounters a window with the <b>WS_EX_CONTROLPARENT</b> style, the system recursively searches the window's children.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getnextdlgtabitem">GetNextDlgTabItem</a>



<b>Reference</b>