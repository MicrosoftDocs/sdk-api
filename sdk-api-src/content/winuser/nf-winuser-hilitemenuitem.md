---
UID: NF:winuser.HiliteMenuItem
title: HiliteMenuItem function (winuser.h)
description: Adds or removes highlighting from an item in a menu bar.
helpviewer_keywords: ["HiliteMenuItem","HiliteMenuItem function [Menus and Other Resources]","MF_BYCOMMAND","MF_BYPOSITION","MF_HILITE","MF_UNHILITE","_win32_HiliteMenuItem","_win32_hilitemenuitem_cpp","menurc.hilitemenuitem","winui._win32_hilitemenuitem","winuser/HiliteMenuItem"]
old-location: menurc\hilitemenuitem.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\hilitemenuitem.htm
ms.date: 12/05/2018
ms.keywords: HiliteMenuItem, HiliteMenuItem function [Menus and Other Resources], MF_BYCOMMAND, MF_BYPOSITION, MF_HILITE, MF_UNHILITE, _win32_HiliteMenuItem, _win32_hilitemenuitem_cpp, menurc.hilitemenuitem, winui._win32_hilitemenuitem, winuser/HiliteMenuItem
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
 - HiliteMenuItem
 - winuser/HiliteMenuItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-menu-l1-1-3.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - ext-ms-win-ntuser-menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-0.dll
 - User32.dll
api_name:
 - HiliteMenuItem
---

# HiliteMenuItem function


## -description

Adds or removes highlighting from an item in a menu bar.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window that contains the menu.

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu bar that contains the item.

### -param uIDHiliteItem [in]

Type: <b>UINT</b>

The menu item. This parameter is either the identifier of the menu item or the offset of the menu item in the menu bar, depending on the value of the <i>uHilite</i> parameter.

### -param uHilite [in]

Type: <b>UINT</b>

Controls the interpretation of the <i>uItemHilite</i> parameter and indicates whether the menu item is highlighted. This parameter must be a combination of either <b>MF_BYCOMMAND</b> or <b>MF_BYPOSITION</b> and <b>MF_HILITE</b> or <b>MF_UNHILITE</b>. 

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
Indicates that <i>uItemHilite</i> gives the identifier of the menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uItemHilite</i> gives the zero-based relative position of the menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_HILITE"></a><a id="mf_hilite"></a><dl>
<dt><b>MF_HILITE</b></dt>
<dt>0x00000080L</dt>
</dl>
</td>
<td width="60%">
Highlights the menu item. If this flag is not specified, the highlighting is removed from the item.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_UNHILITE"></a><a id="mf_unhilite"></a><dl>
<dt><b>MF_UNHILITE</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Removes highlighting from the menu item.

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the menu item is set to the specified highlight state, the return value is nonzero.

If the menu item is not set to the specified highlight state, the return value is zero.

## -remarks

The <b>MF_HILITE</b> and <b>MF_UNHILITE</b> flags can be used only with the <b>HiliteMenuItem</b> function; they cannot be used with the <a href="/windows/desktop/api/winuser/nf-winuser-modifymenua">ModifyMenu</a> function.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/menus">Menus</a>



<a href="/windows/desktop/api/winuser/nf-winuser-modifymenua">ModifyMenu</a>



<b>Reference</b>