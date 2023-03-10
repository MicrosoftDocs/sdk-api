---
UID: NS:winuser.tagMENUBARINFO
title: MENUBARINFO (winuser.h)
description: Contains menu bar information.
helpviewer_keywords: ["*LPMENUBARINFO","*PMENUBARINFO","MENUBARINFO","MENUBARINFO structure [Menus and Other Resources]","PMENUBARINFO","PMENUBARINFO structure pointer [Menus and Other Resources]","_win32_MENUBARINFO_str","_win32_menubarinfo_str_cpp","menurc.menubarinfo","winui._win32_menubarinfo_str","winuser/MENUBARINFO","winuser/PMENUBARINFO"]
old-location: menurc\menubarinfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\menubarinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPMENUBARINFO, *PMENUBARINFO, MENUBARINFO, MENUBARINFO structure [Menus and Other Resources], PMENUBARINFO, PMENUBARINFO structure pointer [Menus and Other Resources], _win32_MENUBARINFO_str, _win32_menubarinfo_str_cpp, menurc.menubarinfo, winui._win32_menubarinfo_str, winuser/MENUBARINFO, winuser/PMENUBARINFO'
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
req.typenames: MENUBARINFO, *PMENUBARINFO, *LPMENUBARINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMENUBARINFO
 - winuser/tagMENUBARINFO
 - PMENUBARINFO
 - winuser/PMENUBARINFO
 - MENUBARINFO
 - winuser/MENUBARINFO
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
 - MENUBARINFO
---

# MENUBARINFO structure


## -description

Contains menu bar information.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. The caller must set this to <code>sizeof(MENUBARINFO)</code>.

### -field rcBar

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The coordinates of the menu bar, popup menu, or menu item.

### -field hMenu

Type: <b>HMENU</b>

A handle to the menu bar or popup menu.

### -field hwndMenu

Type: <b>HWND</b>

A handle to the submenu.

### -field fBarFocused

Type: <b>BOOL</b>

If the menu bar or popup menu has the focus, this member is <b>TRUE</b>. Otherwise, the member is <b>FALSE</b>.

### -field fFocused

Type: <b>BOOL</b>

If the menu item has the focus, this member is <b>TRUE</b>. Otherwise, the member is <b>FALSE</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmenubarinfo">GetMenuBarInfo</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>