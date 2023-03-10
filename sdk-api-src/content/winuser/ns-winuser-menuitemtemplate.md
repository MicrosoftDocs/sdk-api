---
UID: NS:winuser.MENUITEMTEMPLATE
title: MENUITEMTEMPLATE (winuser.h)
description: Defines a menu item in a menu template.
helpviewer_keywords: ["*PMENUITEMTEMPLATE","MENUITEMTEMPLATE","MENUITEMTEMPLATE structure [Menus and Other Resources]","MF_CHECKED","MF_GRAYED","MF_HELP","MF_MENUBARBREAK","MF_MENUBREAK","MF_OWNERDRAW","MF_POPUP","PMENUITEMTEMPLATE","PMENUITEMTEMPLATE structure pointer [Menus and Other Resources]","_win32_MENUITEMTEMPLATE_str","_win32_menuitemtemplate_str_cpp","menurc.menuitemtemplate","winui._win32_menuitemtemplate_str","winuser/MENUITEMTEMPLATE","winuser/PMENUITEMTEMPLATE"]
old-location: menurc\menuitemtemplate.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\menuitemtemplate.htm
ms.date: 12/05/2018
ms.keywords: '*PMENUITEMTEMPLATE, MENUITEMTEMPLATE, MENUITEMTEMPLATE structure [Menus and Other Resources], MF_CHECKED, MF_GRAYED, MF_HELP, MF_MENUBARBREAK, MF_MENUBREAK, MF_OWNERDRAW, MF_POPUP, PMENUITEMTEMPLATE, PMENUITEMTEMPLATE structure pointer [Menus and Other Resources], _win32_MENUITEMTEMPLATE_str, _win32_menuitemtemplate_str_cpp, menurc.menuitemtemplate, winui._win32_menuitemtemplate_str, winuser/MENUITEMTEMPLATE, winuser/PMENUITEMTEMPLATE'
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
req.typenames: MENUITEMTEMPLATE, *PMENUITEMTEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMENUITEMTEMPLATE
 - winuser/PMENUITEMTEMPLATE
 - MENUITEMTEMPLATE
 - winuser/MENUITEMTEMPLATE
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
 - MENUITEMTEMPLATE
---

# MENUITEMTEMPLATE structure


## -description

Defines a menu item in a menu template.

## -struct-fields

### -field mtOption

Type: <b>WORD</b>

One or more of the following predefined menu options that control the appearance of the menu item as shown in the following table. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_CHECKED"></a><a id="mf_checked"></a><dl>
<dt><b>MF_CHECKED</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item has a check mark next to it.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_GRAYED"></a><a id="mf_grayed"></a><dl>
<dt><b>MF_GRAYED</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is initially inactive and drawn with a gray effect.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_HELP"></a><a id="mf_help"></a><dl>
<dt><b>MF_HELP</b></dt>
<dt>0x00004000L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item has a vertical separator to its left.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_MENUBARBREAK"></a><a id="mf_menubarbreak"></a><dl>
<dt><b>MF_MENUBARBREAK</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is placed in a new column. The old and new columns are separated by a bar.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_MENUBREAK"></a><a id="mf_menubreak"></a><dl>
<dt><b>MF_MENUBREAK</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is placed in a new column.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_OWNERDRAW"></a><a id="mf_ownerdraw"></a><dl>
<dt><b>MF_OWNERDRAW</b></dt>
<dt>0x00000100L</dt>
</dl>
</td>
<td width="60%">
Indicates that the owner window of the menu is responsible for drawing all visual aspects of the menu item, including highlighted, selected, and inactive states. This option is not valid for an item in a menu bar.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_POPUP"></a><a id="mf_popup"></a><dl>
<dt><b>MF_POPUP</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
Indicates that the item is one that opens a drop-down menu or submenu.

</td>
</tr>
</table>

### -field mtID

Type: <b>WORD</b>

The menu item identifier of a command item; a command item sends a command message to its owner window. The <b>MENUITEMTEMPLATE</b> structure for an item that opens a drop-down menu or submenu does not contain the 
					<b>mtID</b> member.

### -field mtString

Type: <b>WCHAR[1]</b>

The menu item.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-loadmenuindirecta">LoadMenuIndirect</a>



<a href="/windows/desktop/api/winuser/ns-winuser-menuitemtemplateheader">MENUITEMTEMPLATEHEADER</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>

