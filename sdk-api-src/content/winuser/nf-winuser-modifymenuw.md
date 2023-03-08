---
UID: NF:winuser.ModifyMenuW
title: ModifyMenuW function (winuser.h)
description: Changes an existing menu item. (Unicode)
helpviewer_keywords: ["MF_BITMAP", "MF_BYCOMMAND", "MF_BYPOSITION", "MF_CHECKED", "MF_DISABLED", "MF_ENABLED", "MF_GRAYED", "MF_MENUBARBREAK", "MF_MENUBREAK", "MF_OWNERDRAW", "MF_POPUP", "MF_SEPARATOR", "MF_STRING", "MF_UNCHECKED", "ModifyMenu", "ModifyMenu function [Menus and Other Resources]", "ModifyMenuW", "_win32_ModifyMenu", "_win32_modifymenu_cpp", "menurc.modifymenu", "winui._win32_modifymenu", "winuser/ModifyMenu", "winuser/ModifyMenuW"]
old-location: menurc\modifymenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\modifymenu.htm
ms.date: 12/05/2018
ms.keywords: MF_BITMAP, MF_BYCOMMAND, MF_BYPOSITION, MF_CHECKED, MF_DISABLED, MF_ENABLED, MF_GRAYED, MF_MENUBARBREAK, MF_MENUBREAK, MF_OWNERDRAW, MF_POPUP, MF_SEPARATOR, MF_STRING, MF_UNCHECKED, ModifyMenu, ModifyMenu function [Menus and Other Resources], ModifyMenuA, ModifyMenuW, _win32_ModifyMenu, _win32_modifymenu_cpp, menurc.modifymenu, winui._win32_modifymenu, winuser/ModifyMenu, winuser/ModifyMenuA, winuser/ModifyMenuW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ModifyMenuW (Unicode) and ModifyMenuA (ANSI)
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
 - ModifyMenuW
 - winuser/ModifyMenuW
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
 - ModifyMenu
 - ModifyMenuA
 - ModifyMenuW
req.apiset: ext-ms-win-ntuser-menu-l1-1-3 (introduced in Windows 10, version 10.0.14393)
---

# ModifyMenuW function


## -description

Changes an existing menu item. This function is used to specify the content, appearance, and behavior of the menu item. 
<div class="alert"><b>Note</b>  The <b>ModifyMenu</b> function has been superseded by the <a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a> function. You can still use <b>ModifyMenu</b>, however, if you do not need any of the extended features of <b>SetMenuItemInfo</b>.</div><div> </div>

## -parameters

### -param hMnu [in]

Type: <b>HMENU</b>

A handle to the menu to be changed.

### -param uPosition [in]

Type: <b>UINT</b>

The menu item to be changed, as determined by the <i>uFlags</i> parameter.

### -param uFlags [in]

Type: <b>UINT</b>

Controls the interpretation of the <i>uPosition</i> parameter and the content, appearance, and behavior of the menu item. This parameter must include one of the following required values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_BYCOMMAND"></a><a id="mf_bycommand"></a><dl>
<dt><b>MF_BYCOMMAND</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Indicates that the <i>uPosition</i> parameter gives the identifier of the menu item. The <b>MF_BYCOMMAND</b> flag is the default if neither the <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> flag is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that the <i>uPosition</i> parameter gives the zero-based relative position of the menu item. 

</td>
</tr>
</table>
 

The parameter must also include at least one of the following values.

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
Places a check mark next to the item. If your application provides check-mark bitmaps (see the <a href="/windows/desktop/api/winuser/nf-winuser-setmenuitembitmaps">SetMenuItemBitmaps</a> function), this flag displays a selected bitmap next to the menu item. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_DISABLED"></a><a id="mf_disabled"></a><dl>
<dt><b>MF_DISABLED</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
Disables the menu item so that it cannot be selected, but this flag does not gray it. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_ENABLED"></a><a id="mf_enabled"></a><dl>
<dt><b>MF_ENABLED</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Enables the menu item so that it can be selected and restores it from its grayed state. 

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
Places the item on a new line (for menu bars) or in a new column (for a drop-down menu, submenu, or shortcut menu) without separating columns. 

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
Specifies that the menu item opens a drop-down menu or submenu. The <i>uIDNewItem</i> parameter specifies a handle to the drop-down menu or submenu. This flag is used to add a menu name to a menu bar or a menu item that opens a submenu to a drop-down menu, submenu, or shortcut menu. 

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
Does not place a check mark next to the item (the default). If your application supplies check-mark bitmaps (see the <a href="/windows/desktop/api/winuser/nf-winuser-setmenuitembitmaps">SetMenuItemBitmaps</a> function), this flag displays a clear bitmap next to the menu item. 

</td>
</tr>
</table>

### -param uIDNewItem [in]

Type: <b>UINT_PTR</b>

The identifier of the modified menu item or, if the <i>uFlags</i> parameter has the <b>MF_POPUP</b> flag set, a handle to the drop-down menu or submenu.

### -param lpNewItem [in, optional]

Type: <b>LPCTSTR</b>

The contents of the changed menu item. The interpretation of this parameter depends on whether the <i>uFlags</i> parameter includes the <b>MF_BITMAP</b>, <b>MF_OWNERDRAW</b>, or <b>MF_STRING</b> flag. 

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
A bitmap handle. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_OWNERDRAW"></a><a id="mf_ownerdraw"></a><dl>
<dt><b>MF_OWNERDRAW</b></dt>
<dt>0x00000100L</dt>
</dl>
</td>
<td width="60%">
A value supplied by an application that is used to maintain additional data related to the menu item. The value is in the <b>itemData</b> member of the structure pointed to by the <i>lParam</i> parameter of the <a href="/windows/desktop/Controls/wm-measureitem">WM_MEASUREITEM</a> or <a href="/windows/desktop/Controls/wm-drawitem">WM_DRAWITEM</a> messages sent when the menu item is created or its appearance is updated. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_STRING"></a><a id="mf_string"></a><dl>
<dt><b>MF_STRING</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
A pointer to a null-terminated string (the default). 

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.
                    

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <b>ModifyMenu</b> replaces a menu item that opens a drop-down menu or submenu, the function destroys the old drop-down menu or submenu and frees the memory used by it. 

In order for keyboard accelerators to work with bitmap or owner-drawn menu items, the owner of the menu must process the <a href="/windows/desktop/menurc/wm-menuchar">WM_MENUCHAR</a> message. See <a href="/windows/desktop/menurc/using-menus">Owner-Drawn Menus and the WM_MENUCHAR Message</a> for more information.

The application must call the <a href="/windows/desktop/api/winuser/nf-winuser-drawmenubar">DrawMenuBar</a> function whenever a menu changes, whether the menu is in a displayed window. To change the attributes of existing menu items, it is much faster to use the <a href="/windows/desktop/api/winuser/nf-winuser-checkmenuitem">CheckMenuItem</a> and <a href="/windows/desktop/api/winuser/nf-winuser-enablemenuitem">EnableMenuItem</a> functions. 

The following groups of flags cannot be used together:

				

<ul>
<li><b>MF_BYCOMMAND</b> and <b>MF_BYPOSITION</b></li>
<li><b>MF_DISABLED</b>, <b>MF_ENABLED</b>, and <b>MF_GRAYED</b></li>
<li><b>MF_BITMAP</b>, <b>MF_STRING</b>, <b>MF_OWNERDRAW</b>, and <b>MF_SEPARATOR</b></li>
<li><b>MF_MENUBARBREAK</b> and <b>MF_MENUBREAK</b></li>
<li><b>MF_CHECKED</b> and <b>MF_UNCHECKED</b></li>
</ul>

#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Setting Fonts for Menu-Item Text Strings</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines ModifyMenu as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/menurc/u">AppendMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-checkmenuitem">CheckMenuItem</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-drawmenubar">DrawMenuBar</a>



<a href="/windows/desktop/api/winuser/nf-winuser-enablemenuitem">EnableMenuItem</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuitembitmaps">SetMenuItemBitmaps</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a>
