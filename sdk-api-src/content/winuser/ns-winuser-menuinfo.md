---
UID: NS:winuser.tagMENUINFO
title: MENUINFO (winuser.h)
description: Contains information about a menu.
helpviewer_keywords: ["*LPMENUINFO","LPMENUINFO","LPMENUINFO structure pointer [Menus and Other Resources]","MENUINFO","MENUINFO structure [Menus and Other Resources]","MIM_APPLYTOSUBMENUS","MIM_BACKGROUND","MIM_HELPID","MIM_MAXHEIGHT","MIM_MENUDATA","MIM_STYLE","MNS_AUTODISMISS","MNS_CHECKORBMP","MNS_DRAGDROP","MNS_MODELESS","MNS_NOCHECK","MNS_NOTIFYBYPOS","_win32_MENUINFO_str","_win32_menuinfo_str_cpp","const *LPCMENUINFO","const *LPCMENUINFO structure [Menus and Other Resources]","menurc.menuinfo","winui._win32_menuinfo_str","winuser/LPMENUINFO","winuser/MENUINFO","winuser/const *LPCMENUINFO"]
old-location: menurc\menuinfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\menuinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPMENUINFO, LPMENUINFO, LPMENUINFO structure pointer [Menus and Other Resources], MENUINFO, MENUINFO structure [Menus and Other Resources], MIM_APPLYTOSUBMENUS, MIM_BACKGROUND, MIM_HELPID, MIM_MAXHEIGHT, MIM_MENUDATA, MIM_STYLE, MNS_AUTODISMISS, MNS_CHECKORBMP, MNS_DRAGDROP, MNS_MODELESS, MNS_NOCHECK, MNS_NOTIFYBYPOS, _win32_MENUINFO_str, _win32_menuinfo_str_cpp, const *LPCMENUINFO, const *LPCMENUINFO structure [Menus and Other Resources], menurc.menuinfo, winui._win32_menuinfo_str, winuser/LPMENUINFO, winuser/MENUINFO, winuser/const *LPCMENUINFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MENUINFO, *LPMENUINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMENUINFO
 - winuser/tagMENUINFO
 - LPMENUINFO
 - winuser/LPMENUINFO
 - MENUINFO
 - winuser/MENUINFO
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
 - MENUINFO
---

# MENUINFO structure


## -description

Contains information about a menu.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. The caller must set this member to <code>sizeof(MENUINFO)</code>.

### -field fMask

Type: <b>DWORD</b>

Indicates the members to be retrieved or set (except for <b>MIM_APPLYTOSUBMENUS</b>). This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIM_APPLYTOSUBMENUS"></a><a id="mim_applytosubmenus"></a><dl>
<dt><b>MIM_APPLYTOSUBMENUS</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Settings apply to the menu and all of its submenus. <a href="/windows/desktop/api/winuser/nf-winuser-setmenuinfo">SetMenuInfo</a> uses this flag and <a href="/windows/desktop/api/winuser/nf-winuser-getmenuinfo">GetMenuInfo</a> ignores this flag

</td>
</tr>
<tr>
<td width="40%"><a id="MIM_BACKGROUND"></a><a id="mim_background"></a><dl>
<dt><b>MIM_BACKGROUND</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>hbrBack</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIM_HELPID"></a><a id="mim_helpid"></a><dl>
<dt><b>MIM_HELPID</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>dwContextHelpID</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIM_MAXHEIGHT"></a><a id="mim_maxheight"></a><dl>
<dt><b>MIM_MAXHEIGHT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>cyMax</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIM_MENUDATA"></a><a id="mim_menudata"></a><dl>
<dt><b>MIM_MENUDATA</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>dwMenuData</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="MIM_STYLE"></a><a id="mim_style"></a><dl>
<dt><b>MIM_STYLE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Retrieves or sets the 
						<b>dwStyle</b> member.

</td>
</tr>
</table>

### -field dwStyle

Type: <b>DWORD</b>

The menu style. This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MNS_AUTODISMISS"></a><a id="mns_autodismiss"></a><dl>
<dt><b>MNS_AUTODISMISS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Menu automatically ends when mouse is outside the menu for approximately 10 seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="MNS_CHECKORBMP"></a><a id="mns_checkorbmp"></a><dl>
<dt><b>MNS_CHECKORBMP</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
The same space is reserved for the check mark and the bitmap. If the check mark is drawn, the bitmap is not. All checkmarks and bitmaps are aligned. Used for menus where some items use checkmarks and some use bitmaps.

</td>
</tr>
<tr>
<td width="40%"><a id="MNS_DRAGDROP"></a><a id="mns_dragdrop"></a><dl>
<dt><b>MNS_DRAGDROP</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Menu items are OLE drop targets or drag sources. Menu owner receives <a href="/windows/desktop/menurc/wm-menudrag">WM_MENUDRAG</a> and <a href="/windows/desktop/menurc/wm-menugetobject">WM_MENUGETOBJECT</a> messages.

</td>
</tr>
<tr>
<td width="40%"><a id="MNS_MODELESS"></a><a id="mns_modeless"></a><dl>
<dt><b>MNS_MODELESS</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Menu is modeless; that is, there is no menu modal message loop while the menu is active.

</td>
</tr>
<tr>
<td width="40%"><a id="MNS_NOCHECK"></a><a id="mns_nocheck"></a><dl>
<dt><b>MNS_NOCHECK</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
No space is reserved to the left of an item for a check mark. The item can still be selected, but the check mark will not appear next to the item.

</td>
</tr>
<tr>
<td width="40%"><a id="MNS_NOTIFYBYPOS"></a><a id="mns_notifybypos"></a><dl>
<dt><b>MNS_NOTIFYBYPOS</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
Menu owner receives a <a href="/windows/desktop/menurc/wm-menucommand">WM_MENUCOMMAND</a> message instead of a <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message when the user makes a selection. <b>MNS_NOTIFYBYPOS</b> is a menu header style and has no effect when applied to individual sub menus.

</td>
</tr>
</table>

### -field cyMax

Type: <b>UINT</b>

The maximum height of the menu in pixels. When the menu items exceed the space available, scroll bars are automatically used. The default (0) is the screen height.

### -field hbrBack

Type: <b>HBRUSH</b>

A handle to the brush to be used for the menu's background.

### -field dwContextHelpID

Type: <b>DWORD</b>

The context help identifier. This is the same value used in 
					the <a href="/windows/desktop/api/winuser/nf-winuser-getmenucontexthelpid">GetMenuContextHelpId</a> and 
					<a href="/windows/desktop/api/winuser/nf-winuser-setmenucontexthelpid">SetMenuContextHelpId</a> functions.

### -field dwMenuData

Type: <b>ULONG_PTR</b>

An application-defined value.

## -see-also

<a href="/windows/desktop/menurc/menus">Menus Overview</a>