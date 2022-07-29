---
UID: NF:winuser.SetMenuInfo
title: SetMenuInfo function (winuser.h)
description: Sets information for a specified menu.
helpviewer_keywords: ["SetMenuInfo","SetMenuInfo function [Menus and Other Resources]","_win32_SetMenuInfo","_win32_setmenuinfo_cpp","menurc.setmenuinfo","winui._win32_setmenuinfo","winuser/SetMenuInfo"]
old-location: menurc\setmenuinfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\setmenuinfo.htm
ms.date: 12/05/2018
ms.keywords: SetMenuInfo, SetMenuInfo function [Menus and Other Resources], _win32_SetMenuInfo, _win32_setmenuinfo_cpp, menurc.setmenuinfo, winui._win32_setmenuinfo, winuser/SetMenuInfo
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
 - SetMenuInfo
 - winuser/SetMenuInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetMenuInfo
req.apiset: ext-ms-win-ntuser-menu-l1-1-3 (introduced in Windows 10, version 10.0.14393)
---

# SetMenuInfo function


## -description

Sets information for a specified menu.

## -parameters

### -param unnamedParam1 [in]

Type: <b>HMENU</b>

A handle to a menu.

### -param unnamedParam2 [in]

Type: <b>LPCMENUINFO</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-menuinfo">MENUINFO</a> structure for the menu.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/menurc/menus">Menus</a>
