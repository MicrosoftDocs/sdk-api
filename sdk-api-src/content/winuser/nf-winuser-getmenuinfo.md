---
UID: NF:winuser.GetMenuInfo
title: GetMenuInfo function (winuser.h)
author: windows-sdk-content
description: Retrieves information about a specified menu.
old-location: menurc\getmenuinfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenuinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMenuInfo, GetMenuInfo function [Menus and Other Resources], _win32_GetMenuInfo, _win32_getmenuinfo_cpp, menurc.getmenuinfo, winui._win32_getmenuinfo, winuser/GetMenuInfo
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
api_name:
 - GetMenuInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMenuInfo function


## -description


Retrieves information about a specified menu.


## -parameters




### -param arg1 [in]

Type: <b>HMENU</b>

A handle on a menu. 


### -param arg2 [in, out]

Type: <b>LPMENUINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms647575(v=VS.85).aspx">MENUINFO</a> structure containing information for the menu. Note that you must set the <b>cbSize</b> member to <code>sizeof(MENUINFO)</code> before calling this function. 
				


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>
 

 

