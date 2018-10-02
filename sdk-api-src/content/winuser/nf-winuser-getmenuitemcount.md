---
UID: NF:winuser.GetMenuItemCount
title: GetMenuItemCount function
author: windows-sdk-content
description: Determines the number of items in the specified menu.
old-location: menurc\getmenuitemcount.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenuitemcount.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMenuItemCount, GetMenuItemCount function [Menus and Other Resources], _win32_GetMenuItemCount, _win32_getmenuitemcount_cpp, menurc.getmenuitemcount, winui._win32_getmenuitemcount, winuser/GetMenuItemCount
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
 - GetMenuItemCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMenuItemCount function


## -description


Determines the number of items in the specified menu. 


## -parameters




### -param hMenu [in, optional]

Type: <b>HMENU</b>

A handle to the menu to be examined. 


## -returns



Type: <b>int</b>

If the function succeeds, the return value specifies the number of items in the menu.

If the function fails, the return value is -1. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647979(v=VS.85).aspx">GetMenuItemID</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>
 

 

