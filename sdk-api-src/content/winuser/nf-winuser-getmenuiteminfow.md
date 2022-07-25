---
UID: NF:winuser.GetMenuItemInfoW
title: GetMenuItemInfoW function (winuser.h)
description: Retrieves information about a menu item.
helpviewer_keywords: ["GetMenuItemInfo","GetMenuItemInfo function [Menus and Other Resources]","GetMenuItemInfoA","GetMenuItemInfoW","_win32_GetMenuItemInfo","_win32_getmenuiteminfo_cpp","menurc.getmenuiteminfo","winui._win32_getmenuiteminfo","winuser/GetMenuItemInfo","winuser/GetMenuItemInfoA","winuser/GetMenuItemInfoW"]
old-location: menurc\getmenuiteminfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenuiteminfo.htm
ms.date: 12/05/2018
ms.keywords: GetMenuItemInfo, GetMenuItemInfo function [Menus and Other Resources], GetMenuItemInfoA, GetMenuItemInfoW, _win32_GetMenuItemInfo, _win32_getmenuiteminfo_cpp, menurc.getmenuiteminfo, winui._win32_getmenuiteminfo, winuser/GetMenuItemInfo, winuser/GetMenuItemInfoA, winuser/GetMenuItemInfoW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetMenuItemInfoW (Unicode) and GetMenuItemInfoA (ANSI)
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
 - GetMenuItemInfoW
 - winuser/GetMenuItemInfoW
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
 - GetMenuItemInfo
 - GetMenuItemInfoA
 - GetMenuItemInfoW
req.apiset: ext-ms-win-ntuser-menu-l1-1-3 (introduced in Windows 10, version 10.0.14393)
---

# GetMenuItemInfoW function


## -description

Retrieves information about a menu item.

## -parameters

### -param hmenu [in]

Type: <b>HMENU</b>

A handle to the menu that contains the menu item.

### -param item [in]

Type: <b>UINT</b>

The identifier or position of the menu item to get information about. The meaning of this parameter depends on the value of <i>fByPosition</i>.

### -param fByPosition [in]

Type: <b>BOOL</b>

The meaning of <i>uItem</i>. If this parameter is <b>FALSE</b>, <i>uItem</i> is a menu item identifier. Otherwise, it is a menu item position. See <a href="/windows/desktop/menurc/about-menus">Accessing Menu Items Programmatically</a> for more information.

### -param lpmii [in, out]

Type: <b>LPMENUITEMINFO</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-menuiteminfoa">MENUITEMINFO</a> structure that specifies the information to retrieve and receives information about the menu item. Note that you must set the <b>cbSize</b> member to <code>sizeof(MENUITEMINFO)</code> before calling this function.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

To retrieve a menu item of type <b>MFT_STRING</b>, first find the size of the string by setting the <b>dwTypeData</b> member of <a href="/windows/desktop/api/winuser/ns-winuser-menuiteminfoa">MENUITEMINFO</a> to <b>NULL</b> and then calling <b>GetMenuItemInfo</b>. The value of <b>cch</b>+1 is the size needed. Then allocate a buffer of this size, place the pointer to the buffer in <b>dwTypeData</b>, increment <b>cch</b> by one, and then call <b>GetMenuItemInfo</b> once again to fill the buffer with the string.

If the retrieved menu item is of some other type, then <b>GetMenuItemInfo</b> sets the <b>dwTypeData</b> member to a value whose type is specified by the <b>fType</b><b>fType</b> member and sets <b>cch</b> to 0.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Example of Owner-Drawn Menu Items</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines GetMenuItemInfo as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a>
