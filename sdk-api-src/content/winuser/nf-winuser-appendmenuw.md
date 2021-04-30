---
UID: NF:winuser.AppendMenuW
title: AppendMenuW function (winuser.h)
description: Appends a new item to the end of the specified menu bar, drop-down menu, submenu, or shortcut menu. You can use this function to specify the content, appearance, and behavior of the menu item.
helpviewer_keywords: ["AppendMenu","AppendMenu function [Menus and Other Resources]","AppendMenuA","AppendMenuW","MF_BITMAP","MF_CHECKED","MF_DISABLED","MF_ENABLED","MF_GRAYED","MF_MENUBARBREAK","MF_MENUBREAK","MF_OWNERDRAW","MF_POPUP","MF_SEPARATOR","MF_STRING","MF_UNCHECKED","_win32_AppendMenu","_win32_appendmenu_cpp","menurc.appendmenu","winui._win32_appendmenu","winuser/AppendMenu","winuser/AppendMenuA","winuser/AppendMenuW"]
old-location: menurc\appendmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\appendmenu.htm
ms.date: 12/05/2018
ms.keywords: AppendMenu, AppendMenu function [Menus and Other Resources], AppendMenuA, AppendMenuW, MF_BITMAP, MF_CHECKED, MF_DISABLED, MF_ENABLED, MF_GRAYED, MF_MENUBARBREAK, MF_MENUBREAK, MF_OWNERDRAW, MF_POPUP, MF_SEPARATOR, MF_STRING, MF_UNCHECKED, _win32_AppendMenu, _win32_appendmenu_cpp, menurc.appendmenu, winui._win32_appendmenu, winuser/AppendMenu, winuser/AppendMenuA, winuser/AppendMenuW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AppendMenuW (Unicode) and AppendMenuA (ANSI)
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
 - AppendMenuW
 - winuser/AppendMenuW
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
 - AppendMenu
 - AppendMenuA
 - AppendMenuW
req.apiset: ext-ms-win-ntuser-menu-l1-1-0 (introduced in Windows 8)
---

# AppendMenuW function


## -description

Appends a new item to the end of the specified menu bar, drop-down menu, submenu, or shortcut menu. You can use this function to specify the content, appearance, and behavior of the menu item.

## -parameters

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu bar, drop-down menu, submenu, or shortcut menu to be changed.

### -param uFlags [in]

Type: <b>UINT</b>

Controls the appearance and behavior of the new menu item. This parameter can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_BITMAP"></a><a id="mf_bitmap"></a><dl>
<dt><b>MF_BITMAP</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
Uses a bitmap as the menu item. The <i>lpNewItem</i> parameter contains a handle to the bitmap. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CHECKED"></a><a id="mf_checked"></a><dl>
<dt><b>MF_CHECKED</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
Places a check mark next to the menu item. If the application provides check-mark bitmaps (see <a href="/windows/desktop/api/winuser/nf-winuser-setmenuitembitmaps">SetMenuItemBitmaps</a>, this flag displays the check-mark bitmap next to the menu item. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_DISABLED"></a><a id="mf_disabled"></a><dl>
<dt><b>MF_DISABLED</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
Disables the menu item so that it cannot be selected, but the flag does not gray it. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_ENABLED"></a><a id="mf_enabled"></a><dl>
<dt><b>MF_ENABLED</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Enables the menu item so that it can be selected, and restores it from its grayed state. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_GRAYED"></a><a id="mf_grayed"></a><dl>
<dt><b>MF_GRAYED</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
Disables the menu item and grays it so that it cannot be selected. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_MENUBARBREAK"></a><a id="mf_menubarbreak"></a><dl>
<dt><b>MF_MENUBARBREAK</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
Functions the same as the <b>MF_MENUBREAK</b> flag for a menu bar. For a drop-down menu, submenu, or shortcut menu, the new column is separated from the old column by a vertical line. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_MENUBREAK"></a><a id="mf_menubreak"></a><dl>
<dt><b>MF_MENUBREAK</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td width="60%">
Places the item on a new line (for a menu bar) or in a new column (for a drop-down menu, submenu, or shortcut menu) without separating columns. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_OWNERDRAW"></a><a id="mf_ownerdraw"></a><dl>
<dt><b>MF_OWNERDRAW</b></dt>
<dt>0x00000100L</dt>
</dl>
</td>
<td width="60%">
Specifies that the item is an owner-drawn item. Before the menu is displayed for the first time, the window that owns the menu receives a <a href="/windows/desktop/Controls/wm-measureitem">WM_MEASUREITEM</a> message to retrieve the width and height of the menu item. The <a href="/windows/desktop/Controls/wm-drawitem">WM_DRAWITEM</a> message is then sent to the window procedure of the owner window whenever the appearance of the menu item must be updated. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_POPUP"></a><a id="mf_popup"></a><dl>
<dt><b>MF_POPUP</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
Specifies that the menu item opens a drop-down menu or submenu. The <i>uIDNewItem</i> parameter specifies a handle to the drop-down menu or submenu. This flag is used to add a menu name to a menu bar, or a menu item that opens a submenu to a drop-down menu, submenu, or shortcut menu. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SEPARATOR"></a><a id="mf_separator"></a><dl>
<dt><b>MF_SEPARATOR</b></dt>
<dt>0x00000800L</dt>
</dl>
</td>
<td width="60%">
Draws a horizontal dividing line. This flag is used only in a drop-down menu, submenu, or shortcut menu. The line cannot be grayed, disabled, or highlighted. The <i>lpNewItem</i> and <i>uIDNewItem</i> parameters are ignored. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_STRING"></a><a id="mf_string"></a><dl>
<dt><b>MF_STRING</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Specifies that the menu item is a text string; the <i>lpNewItem</i> parameter is a pointer to the string. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_UNCHECKED"></a><a id="mf_unchecked"></a><dl>
<dt><b>MF_UNCHECKED</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Does not place a check mark next to the item (default). If the application supplies check-mark bitmaps (see <a href="/windows/desktop/api/winuser/nf-winuser-setmenuitembitmaps">SetMenuItemBitmaps</a>), this flag displays the clear bitmap next to the menu item. 

</td>
</tr>
</table>

### -param uIDNewItem [in]

Type: <b>UINT_PTR</b>

The identifier of the new menu item or, if the <i>uFlags</i> parameter is set to <b>MF_POPUP</b>, a handle to the drop-down menu or submenu.

### -param lpNewItem [in, optional]

Type: <b>LPCTSTR</b>

The content of the new menu item. The interpretation of <i>lpNewItem</i> depends on whether the <i>uFlags</i> parameter includes the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_BITMAP"></a><a id="mf_bitmap"></a><dl>
<dt><b>MF_BITMAP</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
Contains a bitmap handle. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_OWNERDRAW"></a><a id="mf_ownerdraw"></a><dl>
<dt><b>MF_OWNERDRAW</b></dt>
<dt>0x00000100L</dt>
</dl>
</td>
<td width="60%">
Contains an application-supplied value that can be used to maintain additional data related to the menu item. The value is in the <b>itemData</b> member of the structure pointed to by the <i>lParam</i> parameter of the <a href="/windows/desktop/Controls/wm-measureitem">WM_MEASUREITEM</a> or <a href="/windows/desktop/Controls/wm-drawitem">WM_DRAWITEM</a> message sent when the menu is created or its appearance is updated. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_STRING"></a><a id="mf_string"></a><dl>
<dt><b>MF_STRING</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Contains a pointer to a null-terminated string. 

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The application must call the <a href="/windows/desktop/api/winuser/nf-winuser-drawmenubar">DrawMenuBar</a> function whenever a menu changes, whether the menu is in a displayed window. 

To get keyboard accelerators to work with bitmap or owner-drawn menu items, the owner of the menu must process the <a href="/windows/desktop/menurc/wm-menuchar">WM_MENUCHAR</a> message. For more information, see <a href="/windows/desktop/menurc/using-menus">Owner-Drawn Menus and the WM_MENUCHAR Message</a>.

The following groups of flags cannot be used together:

<ul>
<li><b>MF_BITMAP</b>, <b>MF_STRING</b>, and <b>MF_OWNERDRAW</b></li>
<li><b>MF_CHECKED</b> and <b>MF_UNCHECKED</b></li>
<li><b>MF_DISABLED</b>, <b>MF_ENABLED</b>, and <b>MF_GRAYED</b></li>
<li><b>MF_MENUBARBREAK</b> and <b>MF_MENUBREAK</b></li>
</ul>

#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Adding Lines and Graphs to a Menu</a>. 

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines AppendMenu as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createmenu">CreateMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-deletemenu">DeleteMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroymenu">DestroyMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-drawmenubar">DrawMenuBar</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insertmenua">InsertMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insertmenuitema">InsertMenuItem</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<a href="/windows/desktop/api/winuser/nf-winuser-modifymenua">ModifyMenu</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-removemenu">RemoveMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuitembitmaps">SetMenuItemBitmaps</a>
