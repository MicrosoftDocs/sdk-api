---
UID: NF:winuser.GetMenuItemID
title: GetMenuItemID function
author: windows-sdk-content
description: Retrieves the menu item identifier of a menu item located at the specified position in a menu.
old-location: menurc\getmenuitemid.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenuitemid.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMenuItemID, GetMenuItemID function [Menus and Other Resources], _win32_GetMenuItemID, _win32_getmenuitemid_cpp, menurc.getmenuitemid, winui._win32_getmenuitemid, winuser/GetMenuItemID
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
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
 - GetMenuItemID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMenuItemID function


## -description


Retrieves the menu item identifier of a menu item located at the specified position in a menu. 


## -parameters




### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu that contains the item whose identifier is to be retrieved. 


### -param nPos [in]

Type: <b>int</b>

The zero-based relative position of the menu item whose identifier is to be retrieved. 


## -returns



Type: <b>UINT</b>

The return value is the identifier of the specified menu item. If the menu item identifier is <b>NULL</b> or if the specified item opens a submenu, the return value is -1. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6a1d542e-b955-48aa-a3b8-e348fefd6f14">GetMenuItemCount</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

