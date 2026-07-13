---
UID: NF:winuser.InsertMenuItemW
title: InsertMenuItemW function (winuser.h)
description: Inserts a new menu item at the specified position in a menu. (Unicode)
helpviewer_keywords: ["InsertMenuItem", "InsertMenuItem function [Menus and Other Resources]", "InsertMenuItemW", "_win32_InsertMenuItem", "_win32_insertmenuitem_cpp", "menurc.insertmenuitem", "winui._win32_insertmenuitem", "winuser/InsertMenuItem", "winuser/InsertMenuItemW"]
old-location: menurc\insertmenuitem.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\insertmenuitem.htm
ms.date: 12/05/2018
ms.keywords: InsertMenuItem, InsertMenuItem function [Menus and Other Resources], InsertMenuItemA, InsertMenuItemW, _win32_InsertMenuItem, _win32_insertmenuitem_cpp, menurc.insertmenuitem, winui._win32_insertmenuitem, winuser/InsertMenuItem, winuser/InsertMenuItemA, winuser/InsertMenuItemW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InsertMenuItemW (Unicode) and InsertMenuItemA (ANSI)
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
 - InsertMenuItemW
 - winuser/InsertMenuItemW
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
 - InsertMenuItem
 - InsertMenuItemA
 - InsertMenuItemW
req.apiset: ext-ms-win-ntuser-menu-l1-1-1 (introduced in Windows 8.1)
---

# InsertMenuItemW function


## -description

Inserts a new menu item at the specified position in a menu.

## -parameters

### -param hmenu [in]

Type: <b>HMENU</b>

A handle to the menu in which the new menu item is inserted.

### -param item [in]

Type: <b>UINT</b>

The identifier or position of the menu item before which to insert the new item. The meaning of this parameter depends on the value of <i>fByPosition</i>.

### -param fByPosition [in]

Type: <b>BOOL</b>

Controls the meaning of <i>item</i>. If this parameter is <b>FALSE</b>, <i>item</i> is a menu item identifier. Otherwise, it is a menu item position. See <a href="/windows/desktop/menurc/about-menus">Accessing Menu Items Programmatically</a> for more information.

### -param lpmi [in]

Type: <b>LPCMENUITEMINFO</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-menuiteminfoa">MENUITEMINFO</a> structure that contains information about the new menu item.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The application must call the <a href="/windows/desktop/api/winuser/nf-winuser-drawmenubar">DrawMenuBar</a> function whenever a menu changes, whether the menu is in a displayed window.

In order for keyboard accelerators to work with bitmap or owner-drawn menu items, the owner of the menu must process the <a href="/windows/desktop/menurc/wm-menuchar">WM_MENUCHAR</a> message. See <a href="/windows/desktop/menurc/using-menus">Owner-Drawn Menus and the WM_MENUCHAR Message</a> for more information.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Example of Menu-Item Bitmaps</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines InsertMenuItem as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-drawmenubar">DrawMenuBar</a>



<a href="/windows/desktop/api/winuser/ns-winuser-menuiteminfoa">MENUITEMINFO</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
