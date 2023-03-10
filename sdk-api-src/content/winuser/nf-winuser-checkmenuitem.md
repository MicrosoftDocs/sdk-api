---
UID: NF:winuser.CheckMenuItem
title: CheckMenuItem function (winuser.h)
description: Sets the state of the specified menu item's check-mark attribute to either selected or clear.
helpviewer_keywords: ["CheckMenuItem","CheckMenuItem function [Menus and Other Resources]","MF_BYCOMMAND","MF_BYPOSITION","MF_CHECKED","MF_UNCHECKED","_win32_CheckMenuItem","_win32_checkmenuitem_cpp","menurc.checkmenuitem","winui._win32_checkmenuitem","winuser/CheckMenuItem"]
old-location: menurc\checkmenuitem.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\checkmenuitem.htm
ms.date: 12/05/2018
ms.keywords: CheckMenuItem, CheckMenuItem function [Menus and Other Resources], MF_BYCOMMAND, MF_BYPOSITION, MF_CHECKED, MF_UNCHECKED, _win32_CheckMenuItem, _win32_checkmenuitem_cpp, menurc.checkmenuitem, winui._win32_checkmenuitem, winuser/CheckMenuItem
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
 - CheckMenuItem
 - winuser/CheckMenuItem
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
 - CheckMenuItem
req.apiset: ext-ms-win-ntuser-menu-l1-1-0 (introduced in Windows 8)
---

# CheckMenuItem function


## -description

<p class="CCE_Message">[<b>CheckMenuItem</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a>.
]

Sets the state of the specified menu item's check-mark attribute to either selected or clear.

## -parameters

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu of interest.

### -param uIDCheckItem [in]

Type: <b>UINT</b>

The menu item whose check-mark attribute is to be set, as determined by the <i>uCheck</i> parameter.

### -param uCheck [in]

Type: <b>UINT</b>

The flags that control the interpretation of the <i>uIDCheckItem</i> parameter and the state of the menu item's check-mark attribute. This parameter can be a combination of either <b>MF_BYCOMMAND</b>, or <b>MF_BYPOSITION</b> and <b>MF_CHECKED</b> or <b>MF_UNCHECKED</b>. 

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
Indicates that the <i>uIDCheckItem</i> parameter gives the identifier of the menu item. The <b>MF_BYCOMMAND</b> flag is the default, if neither the <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> flag is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that the <i>uIDCheckItem</i> parameter gives the zero-based relative position of the menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CHECKED"></a><a id="mf_checked"></a><dl>
<dt><b>MF_CHECKED</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
Sets the check-mark attribute to the selected state.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_UNCHECKED"></a><a id="mf_unchecked"></a><dl>
<dt><b>MF_UNCHECKED</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Sets the check-mark attribute to the clear state.

</td>
</tr>
</table>

## -returns

Type: <b>DWORD</b>

The return value specifies the previous state of the menu item (either <b>MF_CHECKED</b> or <b>MF_UNCHECKED</b>). If the menu item does not exist, the return value is –1.

## -remarks

An item in a menu bar cannot have a check mark. 

The <i>uIDCheckItem</i> parameter identifies a item that opens a submenu or a command item. For a item that opens a submenu, the <i>uIDCheckItem</i> parameter must specify the position of the item. For a command item, the <i>uIDCheckItem</i> parameter can specify either the item's position or its identifier.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Simulating Check Boxes in a Menu</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enablemenuitem">EnableMenuItem</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenuitemid">GetMenuItemID</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuitembitmaps">SetMenuItemBitmaps</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuiteminfoa">SetMenuItemInfo</a>
