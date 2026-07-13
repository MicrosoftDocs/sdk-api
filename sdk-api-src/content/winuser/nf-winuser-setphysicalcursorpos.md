---
UID: NF:winuser.SetPhysicalCursorPos
title: SetPhysicalCursorPos function (winuser.h)
description: Sets the position of the cursor in physical coordinates.
helpviewer_keywords: ["SetPhysicalCursorPos","SetPhysicalCursorPos function [Menus and Other Resources]","_win32_SetPhysicalCursorPos","_win32_setphysicalcursorpos_cpp","menurc.setphysicalcursorpos","winui._win32_setphysicalcursorpos","winuser/SetPhysicalCursorPos"]
old-location: menurc\setphysicalcursorpos.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\setphysicalcursorpos.htm
ms.date: 12/05/2018
ms.keywords: SetPhysicalCursorPos, SetPhysicalCursorPos function [Menus and Other Resources], _win32_SetPhysicalCursorPos, _win32_setphysicalcursorpos_cpp, menurc.setphysicalcursorpos, winui._win32_setphysicalcursorpos, winuser/SetPhysicalCursorPos
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - SetPhysicalCursorPos
 - winuser/SetPhysicalCursorPos
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-gui-l1-3-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - SetPhysicalCursorPos
req.apiset: ext-ms-win-ntuser-gui-l1-1-1 (introduced in Windows 8.1)
---

# SetPhysicalCursorPos function


## -description

Sets the position of the cursor in physical coordinates.

## -parameters

### -param X [in]

Type: <b>int</b>

The new x-coordinate of the cursor, in physical coordinates.

### -param Y [in]

Type: <b>int</b>

The new y-coordinate of the cursor, in physical coordinates.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise <b>FALSE</b>.

## -remarks

For a description of the difference between logical coordinates and physical coordinates, see <a href="/windows/desktop/api/winuser/nf-winuser-physicaltologicalpoint">PhysicalToLogicalPoint</a>.


<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be called to get more information about any error that is generated.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-clipcursor">ClipCursor</a>



<b>Conceptual</b>



<a href="/windows/desktop/menurc/cursors">Cursors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getcursorpos">GetCursorPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos">GetPhysicalCursorPos</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcaretpos">SetCaretPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursorpos">SetCursorPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-showcursor">ShowCursor</a>
