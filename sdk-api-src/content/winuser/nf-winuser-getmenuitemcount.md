---
UID: NF:winuser.GetMenuItemCount
title: GetMenuItemCount function (winuser.h)
description: Determines the number of items in the specified menu.
helpviewer_keywords: ["GetMenuItemCount","GetMenuItemCount function [Menus and Other Resources]","_win32_GetMenuItemCount","_win32_getmenuitemcount_cpp","menurc.getmenuitemcount","winui._win32_getmenuitemcount","winuser/GetMenuItemCount"]
old-location: menurc\getmenuitemcount.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenuitemcount.htm
ms.date: 12/05/2018
ms.keywords: GetMenuItemCount, GetMenuItemCount function [Menus and Other Resources], _win32_GetMenuItemCount, _win32_getmenuitemcount_cpp, menurc.getmenuitemcount, winui._win32_getmenuitemcount, winuser/GetMenuItemCount
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
 - GetMenuItemCount
 - winuser/GetMenuItemCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-0.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - GetMenuItemCount
req.apiset: ext-ms-win-ntuser-menu-l1-1-0 (introduced in Windows 8)
---

# GetMenuItemCount function


## -description

Determines the number of items in the specified menu.

## -parameters

### -param hMenu [in, optional]

Type: <b>HMENU</b>

A handle to the menu to be examined.

## -returns

Type: <b>int</b>

If the function succeeds, the return value specifies the number of items in the menu.

If the function fails, the return value is -1. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenuitemid">GetMenuItemID</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
