---
UID: NF:winuser.GetMenuState
title: GetMenuState function (winuser.h)
description: Retrieves the menu flags associated with the specified menu item.
helpviewer_keywords: ["GetMenuState","GetMenuState function [Menus and Other Resources]","MF_BYCOMMAND","MF_BYPOSITION","_win32_GetMenuState","_win32_getmenustate_cpp","menurc.getmenustate","winui._win32_getmenustate","winuser/GetMenuState"]
old-location: menurc\getmenustate.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenustate.htm
ms.date: 12/05/2018
ms.keywords: GetMenuState, GetMenuState function [Menus and Other Resources], MF_BYCOMMAND, MF_BYPOSITION, _win32_GetMenuState, _win32_getmenustate_cpp, menurc.getmenustate, winui._win32_getmenustate, winuser/GetMenuState
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
 - GetMenuState
 - winuser/GetMenuState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - GetMenuState
req.apiset: ext-ms-win-ntuser-menu-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# GetMenuState function


## -description

Retrieves the menu flags associated with the specified menu item. If the menu item opens a submenu, this function also returns the number of items in the submenu. 
<div class="alert"><b>Note</b>  The <b>GetMenuState</b> function has been superseded by the <a href="/windows/desktop/api/winuser/nf-winuser-getmenuiteminfoa">GetMenuItemInfo</a>. You can still use <b>GetMenuState</b>, however, if you do not need any of the extended features of <b>GetMenuItemInfo</b>.</div><div> </div>

## -parameters

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu that contains the menu item whose flags are to be retrieved.

### -param uId [in]

Type: <b>UINT</b>

The menu item for which the menu flags are to be retrieved, as determined by the <i>uFlags</i> parameter.

### -param uFlags [in]

Type: <b>UINT</b>

Indicates how the <i>uId</i> parameter is interpreted. This parameter can be one of the following values. 

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
Indicates that the <i>uId</i> parameter gives the identifier of the menu item. The <b>MF_BYCOMMAND</b> flag is the default if neither the <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> flag is specified. 

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that the <i>uId</i> parameter gives the zero-based relative position of the menu item. 

</td>
</tr>
</table>

## -returns

Type: <b>UINT</b>

If the specified item does not exist, the return value is -1.

If the menu item opens a submenu, the low-order byte of the return value contains the menu flags associated with the item, and the high-order byte contains the number of items in the submenu opened by the item. 

Otherwise, the return value is a mask (Bitwise OR) of the menu flags. Following are the menu flags associated with the menu item.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_CHECKED</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
A check mark is placed next to the item (for drop-down menus, submenus, and shortcut menus only). 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_DISABLED</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
The item is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_GRAYED</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
The item is disabled and grayed. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_HILITE</b></dt>
<dt>0x00000080L</dt>
</dl>
</td>
<td width="60%">
The item is highlighted. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_MENUBARBREAK</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
This is the same as the <b>MF_MENUBREAK</b> flag, except for drop-down menus, submenus, and shortcut menus, where the new column is separated from the old column by a vertical line. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_MENUBREAK</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td width="60%">
The item is placed on a new line (for menu bars) or in a new column (for drop-down menus, submenus, and shortcut menus) without separating columns. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_OWNERDRAW</b></dt>
<dt>0x00000100L</dt>
</dl>
</td>
<td width="60%">
The item is owner-drawn.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_POPUP</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
Menu item is a submenu.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_SEPARATOR</b></dt>
<dt>0x00000800L</dt>
</dl>
</td>
<td width="60%">
There is a horizontal dividing line (for drop-down menus, submenus, and shortcut menus only). 

</td>
</tr>
</table>

## -remarks

It is possible to test an item for a flag value of <b>MF_ENABLED</b>, <b>MF_STRING</b>, <b>MF_UNCHECKED</b>, or <b>MF_UNHILITE</b>. However, since these values equate to zero you must use an expression to test for them.

				

<table class="clsStd">
<tr>
<th>Flag </th>
<th>Expression to test for the flag</th>
</tr>
<tr>
<td><b>MF_ENABLED</b></td>
<td><code>! (Flag&amp;(MF_DISABLED | MF_GRAYED))</code></td>
</tr>
<tr>
<td><b>MF_STRING</b></td>
<td><code>! (Flag&amp;(MF_BITMAP | MF_OWNERDRAW))</code></td>
</tr>
<tr>
<td><b>MF_UNCHECKED</b></td>
<td><code>! (Flag&amp;MF_CHECKED)</code></td>
</tr>
<tr>
<td><b>MF_UNHILITE</b></td>
<td><code>! (Flag&amp;HILITE)</code></td>
</tr>
</table>
 


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Simulating Check Boxes in a Menu</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenu">GetMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenuitemcount">GetMenuItemCount</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenuitemid">GetMenuItemID</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenuiteminfoa">GetMenuItemInfo</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
