---
UID: NS:winuser.tagMENUITEMINFOW
title: MENUITEMINFOW (winuser.h)
description: Contains information about a menu item. (MENUITEMINFOW)
helpviewer_keywords: ["*LPMENUITEMINFOW","HBMMENU_CALLBACK","HBMMENU_MBAR_CLOSE","HBMMENU_MBAR_CLOSE_D","HBMMENU_MBAR_MINIMIZE","HBMMENU_MBAR_MINIMIZE_D","HBMMENU_MBAR_RESTORE","HBMMENU_POPUP_CLOSE","HBMMENU_POPUP_MAXIMIZE","HBMMENU_POPUP_MINIMIZE","HBMMENU_POPUP_RESTORE","HBMMENU_SYSTEM","LPMENUITEMINFO","LPMENUITEMINFO structure pointer [Menus and Other Resources]","MENUITEMINFO","MENUITEMINFO structure [Menus and Other Resources]","MENUITEMINFOA","MENUITEMINFOW","MFS_CHECKED","MFS_DEFAULT","MFS_DISABLED","MFS_ENABLED","MFS_GRAYED","MFS_HILITE","MFS_UNCHECKED","MFS_UNHILITE","MFT_BITMAP","MFT_MENUBARBREAK","MFT_MENUBREAK","MFT_OWNERDRAW","MFT_RADIOCHECK","MFT_RIGHTJUSTIFY","MFT_RIGHTORDER","MFT_SEPARATOR","MFT_STRING","MIIM_BITMAP","MIIM_CHECKMARKS","MIIM_DATA","MIIM_FTYPE","MIIM_ID","MIIM_STATE","MIIM_STRING","MIIM_SUBMENU","MIIM_TYPE","_win32_MENUITEMINFO_str","_win32_menuiteminfo_str_cpp","menurc.menuiteminfo","winui._win32_menuiteminfo_str","winuser/LPMENUITEMINFO","winuser/MENUITEMINFO","winuser/MENUITEMINFOA","winuser/MENUITEMINFOW"]
old-location: menurc\menuiteminfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\menuiteminfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPMENUITEMINFOW, HBMMENU_CALLBACK, HBMMENU_MBAR_CLOSE, HBMMENU_MBAR_CLOSE_D, HBMMENU_MBAR_MINIMIZE, HBMMENU_MBAR_MINIMIZE_D, HBMMENU_MBAR_RESTORE, HBMMENU_POPUP_CLOSE, HBMMENU_POPUP_MAXIMIZE, HBMMENU_POPUP_MINIMIZE, HBMMENU_POPUP_RESTORE, HBMMENU_SYSTEM, LPMENUITEMINFO, LPMENUITEMINFO structure pointer [Menus and Other Resources], MENUITEMINFO, MENUITEMINFO structure [Menus and Other Resources], MENUITEMINFOA, MENUITEMINFOW, MFS_CHECKED, MFS_DEFAULT, MFS_DISABLED, MFS_ENABLED, MFS_GRAYED, MFS_HILITE, MFS_UNCHECKED, MFS_UNHILITE, MFT_BITMAP, MFT_MENUBARBREAK, MFT_MENUBREAK, MFT_OWNERDRAW, MFT_RADIOCHECK, MFT_RIGHTJUSTIFY, MFT_RIGHTORDER, MFT_SEPARATOR, MFT_STRING, MIIM_BITMAP, MIIM_CHECKMARKS, MIIM_DATA, MIIM_FTYPE, MIIM_ID, MIIM_STATE, MIIM_STRING, MIIM_SUBMENU, MIIM_TYPE, _win32_MENUITEMINFO_str, _win32_menuiteminfo_str_cpp, menurc.menuiteminfo, winui._win32_menuiteminfo_str, winuser/LPMENUITEMINFO, winuser/MENUITEMINFO, winuser/MENUITEMINFOA, winuser/MENUITEMINFOW'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MENUITEMINFOW (Unicode) and MENUITEMINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MENUITEMINFOW, *LPMENUITEMINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMENUITEMINFOW
 - winuser/tagMENUITEMINFOW
 - LPMENUITEMINFOW
 - winuser/LPMENUITEMINFOW
 - MENUITEMINFOW
 - winuser/MENUITEMINFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MENUITEMINFO
 - MENUITEMINFOA
 - MENUITEMINFOW
---

# MENUITEMINFOW structure


## -description

Contains information about a menu item.

## -struct-fields

### -field cbSize

Type: <b>UINT</b>

The size of the structure, in bytes. The caller must set this member to <code>sizeof(MENUITEMINFO)</code>.

### -field fMask

Type: <b>UINT</b>

Indicates the members to be retrieved or set. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIIM_BITMAP"></a><a id="miim_bitmap"></a><dl>
<dt><b>MIIM_BITMAP</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>hbmpItem</b>  member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIIM_CHECKMARKS"></a><a id="miim_checkmarks"></a><dl>
<dt><b>MIIM_CHECKMARKS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>hbmpChecked</b> and  <b>hbmpUnchecked</b> members.

</td>
</tr>
<tr>
<td width="40%"><a id="MIIM_DATA"></a><a id="miim_data"></a><dl>
<dt><b>MIIM_DATA</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>dwItemData</b>  member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIIM_FTYPE"></a><a id="miim_ftype"></a><dl>
<dt><b>MIIM_FTYPE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>fType</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIIM_ID"></a><a id="miim_id"></a><dl>
<dt><b>MIIM_ID</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>wID</b>  member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIIM_STATE"></a><a id="miim_state"></a><dl>
<dt><b>MIIM_STATE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>fState</b>  member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIIM_STRING"></a><a id="miim_string"></a><dl>
<dt><b>MIIM_STRING</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>dwTypeData</b>  member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIIM_SUBMENU"></a><a id="miim_submenu"></a><dl>
<dt><b>MIIM_SUBMENU</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>hSubMenu</b>  member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIIM_TYPE"></a><a id="miim_type"></a><dl>
<dt><b>MIIM_TYPE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>fType</b>  and 
						<b>dwTypeData</b>  members.

<b>MIIM_TYPE</b>  is replaced by <b>MIIM_BITMAP</b>, <b>MIIM_FTYPE</b>, and <b>MIIM_STRING</b>.

</td>
</tr>
</table>

### -field fType

Type: <b>UINT</b>

The menu item type. This member can be one or more of the following values.

The <b>MFT_BITMAP</b>, <b>MFT_SEPARATOR</b>, and <b>MFT_STRING</b> values cannot be combined with one another. Set 
						<b>fMask</b>  to <b>MIIM_TYPE</b>  to use 
						<b>fType</b>.

<b>fType</b> is used only if 
						<b>fMask</b> has a value of <b>MIIM_FTYPE</b>. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFT_BITMAP"></a><a id="mft_bitmap"></a><dl>
<dt><b>MFT_BITMAP</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
Displays the menu item using a bitmap. The low-order word of the 
						<b>dwTypeData</b> member is the bitmap handle, and the 
						<b>cch</b> member is ignored.

<b>MFT_BITMAP</b>  is replaced by <b>MIIM_BITMAP</b> and 
						<b>hbmpItem</b>.
					

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_MENUBARBREAK"></a><a id="mft_menubarbreak"></a><dl>
<dt><b>MFT_MENUBARBREAK</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
Places the menu item on a new line (for a menu bar) or in a new column (for a drop-down menu, submenu, or shortcut menu). For a drop-down menu, submenu, or shortcut menu, a vertical line separates the new column from the old.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_MENUBREAK"></a><a id="mft_menubreak"></a><dl>
<dt><b>MFT_MENUBREAK</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td width="60%">
Places the menu item on a new line (for a menu bar) or in a new column (for a drop-down menu, submenu, or shortcut menu). For a drop-down menu, submenu, or shortcut menu, the columns are not separated by a vertical line.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_OWNERDRAW"></a><a id="mft_ownerdraw"></a><dl>
<dt><b>MFT_OWNERDRAW</b></dt>
<dt>0x00000100L</dt>
</dl>
</td>
<td width="60%">
Assigns responsibility for drawing the menu item to the window that owns the menu. The window receives a <a href="/windows/desktop/Controls/wm-measureitem">WM_MEASUREITEM</a> message before the menu is displayed for the first time, and a <a href="/windows/desktop/Controls/wm-drawitem">WM_DRAWITEM</a> message whenever the appearance of the menu item must be updated. If this value is specified, the 
						<b>dwTypeData</b>   member contains an application-defined value.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_RADIOCHECK"></a><a id="mft_radiocheck"></a><dl>
<dt><b>MFT_RADIOCHECK</b></dt>
<dt>0x00000200L</dt>
</dl>
</td>
<td width="60%">
Displays selected menu items using a radio-button mark instead of a check mark if the 
						<b>hbmpChecked</b> member is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_RIGHTJUSTIFY"></a><a id="mft_rightjustify"></a><dl>
<dt><b>MFT_RIGHTJUSTIFY</b></dt>
<dt>0x00004000L</dt>
</dl>
</td>
<td width="60%">
Right-justifies the menu item and any subsequent items. This value is valid only if the menu item is in a menu bar.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_RIGHTORDER"></a><a id="mft_rightorder"></a><dl>
<dt><b>MFT_RIGHTORDER</b></dt>
<dt>0x00002000L</dt>
</dl>
</td>
<td width="60%">
Specifies that menus cascade right-to-left (the default is left-to-right). This is used to support right-to-left languages, such as Arabic and Hebrew.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_SEPARATOR"></a><a id="mft_separator"></a><dl>
<dt><b>MFT_SEPARATOR</b></dt>
<dt>0x00000800L</dt>
</dl>
</td>
<td width="60%">
Specifies that the menu item is a separator. A menu item separator appears as a horizontal dividing line. The 
						<b>dwTypeData</b>  and 
						<b>cch</b>  members are ignored. This value is valid only in a drop-down menu, submenu, or shortcut menu.

</td>
</tr>
<tr>
<td width="40%"><a id="MFT_STRING"></a><a id="mft_string"></a><dl>
<dt><b>MFT_STRING</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Displays the menu item using a text string. The 
						<b>dwTypeData</b> member is the pointer to a null-terminated string, and the 
						<b>cch</b> member is the length of the string.

<b>MFT_STRING</b> is replaced by <b>MIIM_STRING</b>.

</td>
</tr>
</table>

### -field fState

Type: <b>UINT</b>

The menu item state. This member can be one or more of these values. Set 
					<b>fMask</b> to <b>MIIM_STATE</b> to use 
					<b>fState</b>. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFS_CHECKED"></a><a id="mfs_checked"></a><dl>
<dt><b>MFS_CHECKED</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
Checks the menu item. For more information about selected menu items, see the 
						<b>hbmpChecked</b>  member.

</td>
</tr>
<tr>
<td width="40%"><a id="MFS_DEFAULT"></a><a id="mfs_default"></a><dl>
<dt><b>MFS_DEFAULT</b></dt>
<dt>0x00001000L</dt>
</dl>
</td>
<td width="60%">
Specifies that the menu item is the default. A menu can contain only one default menu item, which is displayed in bold.

</td>
</tr>
<tr>
<td width="40%"><a id="MFS_DISABLED"></a><a id="mfs_disabled"></a><dl>
<dt><b>MFS_DISABLED</b></dt>
<dt>0x00000003L</dt>
</dl>
</td>
<td width="60%">
Disables the menu item and grays it so that it cannot be selected. This is equivalent to <b>MFS_GRAYED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MFS_ENABLED"></a><a id="mfs_enabled"></a><dl>
<dt><b>MFS_ENABLED</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Enables the menu item so that it can be selected. This is the default state.

</td>
</tr>
<tr>
<td width="40%"><a id="MFS_GRAYED"></a><a id="mfs_grayed"></a><dl>
<dt><b>MFS_GRAYED</b></dt>
<dt>0x00000003L</dt>
</dl>
</td>
<td width="60%">
Disables the menu item and grays it so that it cannot be selected. This is equivalent to <b>MFS_DISABLED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MFS_HILITE"></a><a id="mfs_hilite"></a><dl>
<dt><b>MFS_HILITE</b></dt>
<dt>0x00000080L</dt>
</dl>
</td>
<td width="60%">
Highlights the menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="MFS_UNCHECKED"></a><a id="mfs_unchecked"></a><dl>
<dt><b>MFS_UNCHECKED</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Unchecks the menu item. For more information about clear menu items, see the 
						<b>hbmpChecked</b>  member.

</td>
</tr>
<tr>
<td width="40%"><a id="MFS_UNHILITE"></a><a id="mfs_unhilite"></a><dl>
<dt><b>MFS_UNHILITE</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Removes the highlight from the menu item. This is the default state.

</td>
</tr>
</table>

### -field wID

Type: <b>UINT</b>

An application-defined value that identifies the menu item. Set 
					<b>fMask</b>  to <b>MIIM_ID</b>  to use 
					<b>wID</b>.

### -field hSubMenu

Type: <b>HMENU</b>

A handle to the drop-down menu or submenu associated with the menu item. If the menu item is not an item that opens a drop-down menu or submenu, this member is <b>NULL</b>. Set 
					<b>fMask</b>  to <b>MIIM_SUBMENU</b>  to use 
					<b>hSubMenu</b>.

### -field hbmpChecked

Type: <b>HBITMAP</b>

A handle to the bitmap to display next to the item if it is selected. If this member is <b>NULL</b>, a default bitmap is used. If the <b>MFT_RADIOCHECK</b> type value is specified, the default bitmap is a bullet. Otherwise, it is a check mark. Set 
					<b>fMask</b> to <b>MIIM_CHECKMARKS</b> to use 
					<b>hbmpChecked</b>.

### -field hbmpUnchecked

Type: <b>HBITMAP</b>

A handle to the bitmap to display next to the item if it is not selected. If this member is <b>NULL</b>, no bitmap is used. Set 
					<b>fMask</b> to <b>MIIM_CHECKMARKS</b> to use 
					<b>hbmpUnchecked</b>.

### -field dwItemData

Type: <b>ULONG_PTR</b>

An application-defined value associated with the menu item. Set 
					<b>fMask</b> to <b>MIIM_DATA</b> to use 
					<b>dwItemData</b>.

### -field dwTypeData

Type: <b>LPTSTR</b>

The contents of the menu item. The meaning of this member depends on the value of 
					<b>fType</b> and is used only if the <b>MIIM_TYPE</b> flag is set in the 
					<b>fMask</b> member.

To retrieve a menu item of type <b>MFT_STRING</b>, first find the size of the string by setting the 
						<b>dwTypeData</b> member of <b>MENUITEMINFO</b>  to <b>NULL</b> and then calling <a href="/windows/desktop/api/winuser/nf-winuser-getmenuiteminfoa">GetMenuItemInfo</a>. The value of 
						<b>cch</b>+1 is the size needed. Then allocate a buffer of this size, place the pointer to the buffer in 
						<b>dwTypeData</b>, increment <b>cch</b>, and call <b>GetMenuItemInfo</b> once again to fill the buffer with the string. If the retrieved menu item is of some other type, then <b>GetMenuItemInfo</b> sets the 
						<b>dwTypeData</b> member to a value whose type is specified by the 
						<b>fType</b> member.

When using with the <a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a> function, this member should contain a value whose type is specified by the 
						<b>fType</b> member.

<b>dwTypeData</b> is used only if the <b>MIIM_STRING</b> flag is set in the 
						<b>fMask</b> member

### -field cch

Type: <b>UINT</b>

The length of the menu item text, in 
					characters, when information is received about a menu item of the <b>MFT_STRING</b> type. However, <b>cch</b> is used only if the <b>MIIM_TYPE</b> flag is set in the 
					<b>fMask</b> member and is zero otherwise. Also, <b>cch</b> is ignored when the content of a menu item is set by calling <a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a>.

Note that, before calling <a href="/windows/desktop/api/winuser/nf-winuser-getmenuiteminfoa">GetMenuItemInfo</a>, the application must set <b>cch</b> to the length of the buffer pointed to by the 
						<b>dwTypeData</b> member. If the retrieved menu item is of type <b>MFT_STRING</b> (as indicated by the 
						<b>fType</b> member), then <b>GetMenuItemInfo</b> changes 
						<b>cch</b> to the length of the menu item text. If the retrieved menu item is of some other type, <b>GetMenuItemInfo</b> sets the 
						<b>cch</b> field to zero. 

The 
						<b>cch</b> member is used when the <b>MIIM_STRING</b> flag is set in the 
						<b>fMask</b> member.

### -field hbmpItem

Type: <b>HBITMAP</b>

A 
					handle to the bitmap to be displayed, or it can be one of the values in the following table. It is used when the <b>MIIM_BITMAP</b> flag is set in the 
					<b>fMask</b> member. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_CALLBACK"></a><a id="hbmmenu_callback"></a><dl>
<dt><b>HBMMENU_CALLBACK</b></dt>
<dt>((HBITMAP) -1)</dt>
</dl>
</td>
<td width="60%">
A bitmap that is drawn by the window that owns the menu. The application must process the <a href="/windows/desktop/Controls/wm-measureitem">WM_MEASUREITEM</a> and <a href="/windows/desktop/Controls/wm-drawitem">WM_DRAWITEM</a> messages.

</td>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_MBAR_CLOSE"></a><a id="hbmmenu_mbar_close"></a><dl>
<dt><b>HBMMENU_MBAR_CLOSE</b></dt>
<dt>((HBITMAP)  5)</dt>
</dl>
</td>
<td width="60%">
Close button for the menu bar.

</td>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_MBAR_CLOSE_D"></a><a id="hbmmenu_mbar_close_d"></a><dl>
<dt><b>HBMMENU_MBAR_CLOSE_D</b></dt>
<dt>((HBITMAP)  6)</dt>
</dl>
</td>
<td width="60%">
Disabled close button for the menu bar.

</td>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_MBAR_MINIMIZE"></a><a id="hbmmenu_mbar_minimize"></a><dl>
<dt><b>HBMMENU_MBAR_MINIMIZE</b></dt>
<dt>((HBITMAP)  3)</dt>
</dl>
</td>
<td width="60%">
Minimize button for the menu bar.

</td>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_MBAR_MINIMIZE_D"></a><a id="hbmmenu_mbar_minimize_d"></a><dl>
<dt><b>HBMMENU_MBAR_MINIMIZE_D</b></dt>
<dt>((HBITMAP)  7)</dt>
</dl>
</td>
<td width="60%">
Disabled minimize button for the menu bar.

</td>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_MBAR_RESTORE"></a><a id="hbmmenu_mbar_restore"></a><dl>
<dt><b>HBMMENU_MBAR_RESTORE</b></dt>
<dt>((HBITMAP)  2)</dt>
</dl>
</td>
<td width="60%">
Restore button for the menu bar.

</td>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_POPUP_CLOSE"></a><a id="hbmmenu_popup_close"></a><dl>
<dt><b>HBMMENU_POPUP_CLOSE</b></dt>
<dt>((HBITMAP)  8)</dt>
</dl>
</td>
<td width="60%">
Close button for the submenu.

</td>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_POPUP_MAXIMIZE"></a><a id="hbmmenu_popup_maximize"></a><dl>
<dt><b>HBMMENU_POPUP_MAXIMIZE</b></dt>
<dt>((HBITMAP) 10)</dt>
</dl>
</td>
<td width="60%">
Maximize button for the submenu.

</td>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_POPUP_MINIMIZE"></a><a id="hbmmenu_popup_minimize"></a><dl>
<dt><b>HBMMENU_POPUP_MINIMIZE</b></dt>
<dt>((HBITMAP) 11)</dt>
</dl>
</td>
<td width="60%">
Minimize button for the submenu.

</td>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_POPUP_RESTORE"></a><a id="hbmmenu_popup_restore"></a><dl>
<dt><b>HBMMENU_POPUP_RESTORE</b></dt>
<dt>((HBITMAP)  9)</dt>
</dl>
</td>
<td width="60%">
Restore button for the submenu.

</td>
</tr>
<tr>
<td width="40%"><a id="HBMMENU_SYSTEM"></a><a id="hbmmenu_system"></a><dl>
<dt><b>HBMMENU_SYSTEM</b></dt>
<dt>((HBITMAP)  1)</dt>
</dl>
</td>
<td width="60%">
Windows icon or the icon of the window specified in 
						<b>dwItemData</b>.

</td>
</tr>
</table>

## -remarks

The <b>MENUITEMINFO</b> structure is used with the <a href="/windows/desktop/api/winuser/nf-winuser-getmenuiteminfoa">GetMenuItemInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-insertmenuitema">InsertMenuItem</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a> functions.

The menu can display items using text, bitmaps, or both.





> [!NOTE]
> The winuser.h header defines MENUITEMINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenuiteminfoa">GetMenuItemInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insertmenuitema">InsertMenuItem</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a>



<a href="/windows/desktop/Controls/wm-drawitem">WM_DRAWITEM</a>



<a href="/windows/desktop/Controls/wm-measureitem">WM_MEASUREITEM</a>
