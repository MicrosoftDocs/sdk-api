---
UID: NF:winuser.LoadMenuA
title: LoadMenuA function (winuser.h)
description: Loads the specified menu resource from the executable (.exe) file associated with an application instance. (ANSI)
helpviewer_keywords: ["LoadMenuA", "winuser/LoadMenuA"]
old-location: menurc\loadmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\loadmenu.htm
ms.date: 12/05/2018
ms.keywords: LoadMenu, LoadMenu function [Menus and Other Resources], LoadMenuA, LoadMenuW, _win32_LoadMenu, _win32_loadmenu_cpp, menurc.loadmenu, winui._win32_loadmenu, winuser/LoadMenu, winuser/LoadMenuA, winuser/LoadMenuW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadMenuW (Unicode) and LoadMenuA (ANSI)
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
 - LoadMenuA
 - winuser/LoadMenuA
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
 - LoadMenu
 - LoadMenuA
 - LoadMenuW
req.apiset: ext-ms-win-ntuser-menu-l1-1-3 (introduced in Windows 10, version 10.0.14393)
---

# LoadMenuA function


## -description

Loads the specified menu resource from the executable (.exe) file associated with an application instance.

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module containing the menu resource to be loaded.

### -param lpMenuName [in]

Type: <b>LPCTSTR</b>

The name of the menu resource. Alternatively, this parameter can consist of the resource identifier in the low-order word and zero in the high-order word. To create this value, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro.

## -returns

Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the menu resource.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/desktop/api/winuser/nf-winuser-destroymenu">DestroyMenu</a> function is used, before an application closes, to destroy the menu and free memory that the loaded menu occupied. 


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Displaying a Shortcut Menu</a>

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines LoadMenu as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-loadmenuindirecta">LoadMenuIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
