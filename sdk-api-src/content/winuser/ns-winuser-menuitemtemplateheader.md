---
UID: NS:winuser.MENUITEMTEMPLATEHEADER
title: MENUITEMTEMPLATEHEADER (winuser.h)
description: Defines the header for a menu template. A complete menu template consists of a header and one or more menu item lists.
helpviewer_keywords: ["*PMENUITEMTEMPLATEHEADER","MENUITEMTEMPLATEHEADER","MENUITEMTEMPLATEHEADER structure [Menus and Other Resources]","PMENUITEMTEMPLATEHEADER","PMENUITEMTEMPLATEHEADER structure pointer [Menus and Other Resources]","_win32_MENUITEMTEMPLATEHEADER_str","_win32_menuitemtemplateheader_str_cpp","menurc.menuitemtemplateheader","winui._win32_menuitemtemplateheader_str","winuser/MENUITEMTEMPLATEHEADER","winuser/PMENUITEMTEMPLATEHEADER"]
old-location: menurc\menuitemtemplateheader.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\menuitemtemplateheader.htm
ms.date: 12/05/2018
ms.keywords: '*PMENUITEMTEMPLATEHEADER, MENUITEMTEMPLATEHEADER, MENUITEMTEMPLATEHEADER structure [Menus and Other Resources], PMENUITEMTEMPLATEHEADER, PMENUITEMTEMPLATEHEADER structure pointer [Menus and Other Resources], _win32_MENUITEMTEMPLATEHEADER_str, _win32_menuitemtemplateheader_str_cpp, menurc.menuitemtemplateheader, winui._win32_menuitemtemplateheader_str, winuser/MENUITEMTEMPLATEHEADER, winuser/PMENUITEMTEMPLATEHEADER'
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
req.typenames: MENUITEMTEMPLATEHEADER, *PMENUITEMTEMPLATEHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PMENUITEMTEMPLATEHEADER
 - winuser/PMENUITEMTEMPLATEHEADER
 - MENUITEMTEMPLATEHEADER
 - winuser/MENUITEMTEMPLATEHEADER
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
 - MENUITEMTEMPLATEHEADER
---

# MENUITEMTEMPLATEHEADER structure


## -description

Defines the header for a menu template. A complete menu template consists of a header and one or more menu item lists.

## -struct-fields

### -field versionNumber

Type: <b>WORD</b>

The version number. This member must be zero.

### -field offset

Type: <b>WORD</b>

The offset, in bytes, from the end of the header. The menu item list begins at this offset. Usually, this member is zero, and the menu item list follows immediately after the header.

## -remarks

One or more <a href="/windows/desktop/api/winuser/ns-winuser-menuitemtemplate">MENUITEMTEMPLATE</a> structures are combined to form the menu item list.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-loadmenuindirecta">LoadMenuIndirect</a>



<a href="/windows/desktop/api/winuser/ns-winuser-menuitemtemplate">MENUITEMTEMPLATE</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>

