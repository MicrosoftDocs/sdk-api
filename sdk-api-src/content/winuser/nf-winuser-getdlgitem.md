---
UID: NF:winuser.GetDlgItem
title: GetDlgItem function (winuser.h)
description: Retrieves a handle to a control in the specified dialog box.
helpviewer_keywords: ["GetDlgItem","GetDlgItem function [Dialog Boxes]","_win32_GetDlgItem","_win32_getdlgitem_cpp","dlgbox.getdlgitem","winui._win32_getdlgitem","winuser/GetDlgItem"]
old-location: dlgbox\getdlgitem.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getdlgitem.htm
ms.date: 12/05/2018
ms.keywords: GetDlgItem, GetDlgItem function [Dialog Boxes], _win32_GetDlgItem, _win32_getdlgitem_cpp, dlgbox.getdlgitem, winui._win32_getdlgitem, winuser/GetDlgItem
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
 - GetDlgItem
 - winuser/GetDlgItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-dialogbox-l1-1-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-0.dll
 - Ext-MS-Win-NTUser-DialogBox-l1-1-1.dll
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - GetDlgItem
req.apiset: ext-ms-win-ntuser-dialogbox-l1-1-0 (introduced in Windows 8)
---

# GetDlgItem function


## -description

Retrieves a handle to a control in the specified dialog box.

## -parameters

### -param hDlg [in, optional]

Type: <b>HWND</b>

A handle to the dialog box that contains the control.

### -param nIDDlgItem [in]

Type: <b>int</b>

The identifier of the control to be retrieved.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is the window handle of the specified control. 

If the function fails, the return value is <b>NULL</b>, indicating an invalid dialog box handle or a nonexistent control. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You can use the <b>GetDlgItem</b> function with any parent-child window pair, not just with dialog boxes. As long as the <i>hDlg</i> parameter specifies a parent window and the child window has a unique identifier (as specified by the <i>hMenu</i> parameter in the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> or <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function that created the child window), <b>GetDlgItem</b> returns a valid handle to the child window. 


#### Examples

For an example, see <a href="/windows/desktop/dlgbox/using-dialog-boxes">Initializing a Dialog Box</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<a href="/windows/desktop/dlgbox/dialog-boxes">Dialog Boxes</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint">GetDlgItemInt</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta">GetDlgItemText</a>



<b>Reference</b>
