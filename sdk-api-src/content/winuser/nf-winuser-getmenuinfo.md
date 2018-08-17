---
UID: NF:winuser.GetMenuInfo
title: GetMenuInfo function
author: windows-sdk-content
description: Retrieves information about a specified menu.
old-location: menurc\getmenuinfo.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenuinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMenuInfo, GetMenuInfo function [Menus and Other Resources], _win32_GetMenuInfo, _win32_getmenuinfo_cpp, menurc.getmenuinfo, winui._win32_getmenuinfo, winuser/GetMenuInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetMenuInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetMenuInfo function


## -description


Retrieves information about a specified menu.


## -parameters




### -param

TBD




#### - [in]

Type: <b>HMENU</b>

A handle on a menu. 


#### - lpcmi [in, out]

Type: <b>LPMENUINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/dc53a6c7-b75b-4228-b04f-befff07270d4">MENUINFO</a> structure containing information for the menu. Note that you must set the <b>cbSize</b> member to <code>sizeof(MENUINFO)</code> before calling this function. 
				


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>
 

 

