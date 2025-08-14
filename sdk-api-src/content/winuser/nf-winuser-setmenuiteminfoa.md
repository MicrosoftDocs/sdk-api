---
UID: NF:winuser.SetMenuItemInfoA
title: SetMenuItemInfoA function (winuser.h)
description: Changes information about a menu item. (ANSI)
helpviewer_keywords: ["SetMenuItemInfoA", "winuser/SetMenuItemInfoA"]
old-location: menurc\setmenuiteminfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\setmenuiteminfo.htm
ms.date: 07/02/2025
ms.keywords: SetMenuItemInfo, SetMenuItemInfo function [Menus and Other Resources], SetMenuItemInfoA, SetMenuItemInfoW, _win32_SetMenuItemInfo, _win32_setmenuiteminfo_cpp, menurc.setmenuiteminfo, winui._win32_setmenuiteminfo, winuser/SetMenuItemInfo, winuser/SetMenuItemInfoA, winuser/SetMenuItemInfoW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetMenuItemInfoW (Unicode) and SetMenuItemInfoA (ANSI)
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
 - SetMenuItemInfoA
 - winuser/SetMenuItemInfoA
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
 - SetMenuItemInfo
 - SetMenuItemInfoA
 - SetMenuItemInfoW
req.apiset: ext-ms-win-ntuser-menu-l1-1-0 (introduced in Windows 8)
---

# SetMenuItemInfoA function


## -description

Changes information about a menu item.

## -parameters

### -param hmenu [in]

Type: <b>HMENU</b>

A handle to the menu that contains the menu item.

### -param item [in]

Type: <b>UINT</b>

The identifier or position of the menu item to change. The meaning of this parameter depends on the value of <i>fByPositon</i>.

### -param fByPositon [in]

Type: <b>BOOL</b>

The meaning of <i>uItem</i>. If this parameter is <b>FALSE</b>, <i>uItem</i> is a menu item identifier. Otherwise, it is a menu item position. See <a href="/windows/desktop/menurc/about-menus">About Menus</a> for more information. (_Note: this parameter is misspelled in the header; it should be used as shown here._)

### -param lpmii [in]

Type: <b>LPMENUITEMINFO</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-menuiteminfoa">MENUITEMINFO</a> structure that contains information about the menu item and specifies which menu item attributes to change.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The application must call the <a href="/windows/desktop/api/winuser/nf-winuser-drawmenubar">DrawMenuBar</a> function whenever a menu changes, whether the menu is in a displayed window.

In order for keyboard accelerators to work with bitmap or owner-drawn menu items, the owner of the menu must process the <a href="/windows/desktop/menurc/wm-menuchar">WM_MENUCHAR</a> message. See <a href="/windows/desktop/menurc/using-menus">Owner-Drawn Menus and the WM_MENUCHAR Message</a> for more information.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Example of Owner-Drawn Menu Items</a>. 



<div class="code"></div>




> [!NOTE]
> The winuser.h header defines SetMenuItemInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-drawmenubar">DrawMenuBar</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenuiteminfoa">GetMenuItemInfo</a>



<a href="/windows/desktop/api/winuser/ns-winuser-menuiteminfoa">MENUITEMINFO</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
