---
UID: NF:winuser.GetPhysicalCursorPos
title: GetPhysicalCursorPos function (winuser.h)
description: Retrieves the position of the cursor in physical coordinates.
helpviewer_keywords: ["GetPhysicalCursorPos","GetPhysicalCursorPos function [Menus and Other Resources]","_win32_GetPhysicalCursorPos","_win32_getphysicalcursorpos_cpp","menurc.getphysicalcursorpos","winui._win32_getphysicalcursorpos","winuser/GetPhysicalCursorPos"]
old-location: menurc\getphysicalcursorpos.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getphysicalcursorpos.htm
ms.date: 12/05/2018
ms.keywords: GetPhysicalCursorPos, GetPhysicalCursorPos function [Menus and Other Resources], _win32_GetPhysicalCursorPos, _win32_getphysicalcursorpos_cpp, menurc.getphysicalcursorpos, winui._win32_getphysicalcursorpos, winuser/GetPhysicalCursorPos
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
 - GetPhysicalCursorPos
 - winuser/GetPhysicalCursorPos
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
 - GetPhysicalCursorPos
req.apiset: ext-ms-win-ntuser-gui-l1-1-1 (introduced in Windows 8.1)
---

# GetPhysicalCursorPos function


## -description

Retrieves the position of the cursor in physical coordinates.

## -parameters

### -param lpPoint [out]

Type: <b>LPPOINT</b>

The position of the cursor, in physical coordinates.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise <b>FALSE</b>.


<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can be called to get more information about any error that is generated.

## -remarks

For a description of the difference between logical coordinates and physical coordinates, see <a href="/windows/desktop/api/winuser/nf-winuser-physicaltologicalpoint">PhysicalToLogicalPoint</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-clipcursor">ClipCursor</a>



<b>Conceptual</b>



<a href="/windows/desktop/menurc/cursors">Cursors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getcursorpos">GetCursorPos</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcaretpos">SetCaretPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursorpos">SetCursorPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setphysicalcursorpos">SetPhysicalCursorPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-showcursor">ShowCursor</a>
