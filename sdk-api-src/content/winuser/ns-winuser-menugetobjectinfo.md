---
UID: NS:winuser.tagMENUGETOBJECTINFO
title: MENUGETOBJECTINFO (winuser.h)
description: Contains information about the menu that the mouse cursor is on.
helpviewer_keywords: ["*PMENUGETOBJECTINFO","MENUGETOBJECTINFO","MENUGETOBJECTINFO structure [Menus and Other Resources]","MNGOF_BOTTOMGAP","MNGOF_TOPGAP","PMENUGETOBJECTINFO","PMENUGETOBJECTINFO structure pointer [Menus and Other Resources]","_win32_MENUGETOBJECTINFO_str","_win32_menugetobjectinfo_str_cpp","menurc.menugetobjectinfo","winui._win32_menugetobjectinfo_str","winuser/MENUGETOBJECTINFO","winuser/PMENUGETOBJECTINFO"]
old-location: menurc\menugetobjectinfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\menugetobjectinfo.htm
ms.date: 12/05/2018
ms.keywords: '*PMENUGETOBJECTINFO, MENUGETOBJECTINFO, MENUGETOBJECTINFO structure [Menus and Other Resources], MNGOF_BOTTOMGAP, MNGOF_TOPGAP, PMENUGETOBJECTINFO, PMENUGETOBJECTINFO structure pointer [Menus and Other Resources], _win32_MENUGETOBJECTINFO_str, _win32_menugetobjectinfo_str_cpp, menurc.menugetobjectinfo, winui._win32_menugetobjectinfo_str, winuser/MENUGETOBJECTINFO, winuser/PMENUGETOBJECTINFO'
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
req.typenames: MENUGETOBJECTINFO, *PMENUGETOBJECTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMENUGETOBJECTINFO
 - winuser/tagMENUGETOBJECTINFO
 - PMENUGETOBJECTINFO
 - winuser/PMENUGETOBJECTINFO
 - MENUGETOBJECTINFO
 - winuser/MENUGETOBJECTINFO
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
 - MENUGETOBJECTINFO
---

# MENUGETOBJECTINFO structure


## -description

Contains information about the menu that the mouse cursor is on.

## -struct-fields

### -field dwFlags

Type: <b>DWORD</b>

The position of the mouse cursor with respect to the item indicated by 
					<b>uPos</b>. It is a bitmask of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MNGOF_BOTTOMGAP"></a><a id="mngof_bottomgap"></a><dl>
<dt><b>MNGOF_BOTTOMGAP</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The mouse is on the bottom of the item indicated by 
						<b>uPos</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MNGOF_TOPGAP"></a><a id="mngof_topgap"></a><dl>
<dt><b>MNGOF_TOPGAP</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The mouse is on the top of the item indicated by 
						<b>uPos</b>.

</td>
</tr>
</table>
 

If neither MNGOF_BOTTOMGAP nor MNGOF_TOPGAP is set, then the mouse is directly on the item indicated by <b>uPos</b>.

### -field uPos

Type: <b>UINT</b>

The position of the item the mouse cursor is on.

### -field hmenu

Type: <b>HMENU</b>

A handle to the menu the mouse cursor is on.

### -field riid

Type: <b>PVOID</b>

The identifier of the requested interface. Currently it can only be <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>.

### -field pvObj

Type: <b>PVOID</b>

A pointer to the interface corresponding to the 
					<b>riid</b> member. This pointer is to be returned by the application when processing the message.

## -remarks

The <b>MENUGETOBJECTINFO</b> structure is used only in drag-and-drop menus. When the 
				<a href="/windows/desktop/menurc/wm-menugetobject">WM_MENUGETOBJECT</a>  message is sent, 
				<i>lParam</i> is a pointer to this structure. 

To create a drag-and-drop menu, call <a href="/windows/desktop/api/winuser/nf-winuser-setmenuinfo">SetMenuInfo</a> with <b>MNS_DRAGDROP</b> set.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuinfo">SetMenuInfo</a>