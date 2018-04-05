---
UID: NF:winuser.GetSubMenu
title: GetSubMenu function
author: windows-driver-content
description: Retrieves a handle to the drop-down menu or submenu activated by the specified menu item.
old-location: menurc\getsubmenu.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getsubmenu.htm
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: GetSubMenu, GetSubMenu function [Menus and Other Resources], _win32_GetSubMenu, _win32_getsubmenu_cpp, menurc.getsubmenu, winui._win32_getsubmenu, winuser/GetSubMenu
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	Ext-MS-Win-NTUser-Menu-l1-1-0.dll
-	Ext-MS-Win-NTUser-Menu-l1-1-1.dll
-	ext-ms-win-ntuser-menu-l1-1-2.dll
-	Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
-	GetSubMenu
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetSubMenu function


## -description


Retrieves a handle to the drop-down menu or submenu activated by the specified menu item. 


## -parameters




### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu. 


### -param nPos [in]

Type: <b>int</b>

The zero-based relative position in the specified menu of an item that activates a drop-down menu or submenu. 


## -returns



Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the drop-down menu or submenu activated by the menu item. If the menu item does not activate a drop-down menu or submenu, the return value is <b>NULL</b>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b1341fe7-1532-4e0b-82f3-540cc88c0aa7">CreatePopupMenu</a>



<a href="https://msdn.microsoft.com/e86b20c6-9a4b-40b7-95d1-ffa57795f5e0">GetMenu</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

