---
UID: NF:winuser.EnableMenuItem
title: EnableMenuItem function (winuser.h)
description: Enables, disables, or grays the specified menu item.
helpviewer_keywords: ["EnableMenuItem","EnableMenuItem function [Menus and Other Resources]","MF_BYCOMMAND","MF_BYPOSITION","MF_DISABLED","MF_ENABLED","MF_GRAYED","_win32_EnableMenuItem","_win32_enablemenuitem_cpp","menurc.enablemenuitem","winui._win32_enablemenuitem","winuser/EnableMenuItem"]
old-location: menurc\enablemenuitem.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\enablemenuitem.htm
ms.date: 12/05/2018
ms.keywords: EnableMenuItem, EnableMenuItem function [Menus and Other Resources], MF_BYCOMMAND, MF_BYPOSITION, MF_DISABLED, MF_ENABLED, MF_GRAYED, _win32_EnableMenuItem, _win32_enablemenuitem_cpp, menurc.enablemenuitem, winui._win32_enablemenuitem, winuser/EnableMenuItem
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
 - EnableMenuItem
 - winuser/EnableMenuItem
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
 - EnableMenuItem
req.apiset: ext-ms-win-ntuser-menu-l1-1-0 (introduced in Windows 8)
---

# EnableMenuItem function


## -description

Enables, disables, or grays the specified menu item.

## -parameters

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu.

### -param uIDEnableItem [in]

Type: <b>UINT</b>

The menu item to be enabled, disabled, or grayed, as determined by the <i>uEnable</i> parameter. This parameter specifies an item in a menu bar, menu, or submenu.

### -param uEnable [in]

Type: <b>UINT</b>

Controls the interpretation of the <i>uIDEnableItem</i> parameter and indicate whether the menu item is enabled, disabled, or grayed. This parameter must be a combination of the following values. 

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
Indicates that <i>uIDEnableItem</i> gives the identifier of the menu item. If neither the <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> flag is specified, the <b>MF_BYCOMMAND</b> flag is the default flag.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uIDEnableItem</i> gives the zero-based relative position of the menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_DISABLED"></a><a id="mf_disabled"></a><dl>
<dt><b>MF_DISABLED</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is disabled, but not grayed, so it cannot be selected.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_ENABLED"></a><a id="mf_enabled"></a><dl>
<dt><b>MF_ENABLED</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is enabled and restored from a grayed state so that it can be selected.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_GRAYED"></a><a id="mf_grayed"></a><dl>
<dt><b>MF_GRAYED</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is disabled and grayed so that it cannot be selected.

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

The return value specifies the previous state of the menu item (it is either <b>MF_DISABLED</b>, <b>MF_ENABLED</b>, or <b>MF_GRAYED</b>). If the menu item does not exist, the return value is -1.

## -remarks

An application must use the <b>MF_BYPOSITION</b> flag to specify the correct menu handle. If the menu handle to the menu bar is specified, the top-level menu item (an item in the menu bar) is affected. To set the state of an item in a drop-down menu or submenu by position, an application must specify a handle to the drop-down menu or submenu. 

When an application specifies the <b>MF_BYCOMMAND</b> flag, the system checks all items that open submenus in the menu identified by the specified menu handle. Therefore, unless duplicate menu items are present, specifying the menu handle to the menu bar is sufficient. 

The <a href="/windows/desktop/api/winuser/nf-winuser-insertmenua">InsertMenu</a>, <a href="/windows/desktop/api/winuser/nf-winuser-insertmenuitema">InsertMenuItem</a>, <a href="/windows/desktop/api/winuser/nf-winuser-loadmenuindirecta">LoadMenuIndirect</a>, <a href="/windows/desktop/api/winuser/nf-winuser-modifymenua">ModifyMenu</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a> functions can also set the state (enabled, disabled, or grayed) of a menu item.

When you change a window menu, the menu bar is not immediately updated. To force the update, call <a href="/windows/desktop/api/winuser/nf-winuser-drawmenubar">DrawMenuBar</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-drawmenubar">DrawMenuBar</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenuitemid">GetMenuItemID</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insertmenua">InsertMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-insertmenuitema">InsertMenuItem</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadmenuindirecta">LoadMenuIndirect</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<a href="/windows/desktop/api/winuser/nf-winuser-modifymenua">ModifyMenu</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a>



<a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a>
