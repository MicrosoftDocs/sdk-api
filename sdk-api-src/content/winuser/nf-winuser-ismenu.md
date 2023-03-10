---
UID: NF:winuser.IsMenu
title: IsMenu function (winuser.h)
description: Determines whether a handle is a menu handle.
helpviewer_keywords: ["IsMenu","IsMenu function [Menus and Other Resources]","_win32_IsMenu","_win32_ismenu_cpp","menurc.ismenu","winui._win32_ismenu","winuser/IsMenu"]
old-location: menurc\ismenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\ismenu.htm
ms.date: 12/05/2018
ms.keywords: IsMenu, IsMenu function [Menus and Other Resources], _win32_IsMenu, _win32_ismenu_cpp, menurc.ismenu, winui._win32_ismenu, winuser/IsMenu
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
 - IsMenu
 - winuser/IsMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - IsMenu
req.apiset: ext-ms-win-ntuser-menu-l1-1-1 (introduced in Windows 8.1)
---

# IsMenu function


## -description

Determines whether a handle is a menu handle.

## -parameters

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to be tested.

## -returns

Type: <b>BOOL</b>

If the handle is a menu handle, the return value is nonzero. 

If the handle is not a menu handle, the return value is zero.

## -see-also

<a href="/windows/desktop/menurc/menus">Menus</a>
