---
UID: NS:winuser.tagMENUBARINFO
title: tagMENUBARINFO
author: windows-driver-content
description: Contains menu bar information.
old-location: menurc\menubarinfo.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\menubarinfo.htm
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*LPMENUBARINFO, *PMENUBARINFO, MENUBARINFO, MENUBARINFO structure [Menus and Other Resources], PMENUBARINFO, PMENUBARINFO structure pointer [Menus and Other Resources], _win32_MENUBARINFO_str, _win32_menubarinfo_str_cpp, menurc.menubarinfo, tagMENUBARINFO, winui._win32_menubarinfo_str, winuser/MENUBARINFO, winuser/PMENUBARINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: MENUBARINFO, *PMENUBARINFO, *LPMENUBARINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winuser.h
api_name:
-	MENUBARINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagMENUBARINFO structure


## -description


Contains menu bar information.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. The caller must set this to <code>sizeof(MENUBARINFO)</code>. 


### -field rcBar

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

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



<a href="https://msdn.microsoft.com/552868df-9641-4584-bbd1-89c8c5806a68">GetMenuBarInfo</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<b>Reference</b>
 

 

