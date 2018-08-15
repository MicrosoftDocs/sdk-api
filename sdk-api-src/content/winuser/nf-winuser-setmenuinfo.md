---
UID: NF:winuser.SetMenuInfo
title: SetMenuInfo function
author: windows-sdk-content
description: Sets information for a specified menu.
old-location: menurc\setmenuinfo.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\setmenuinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetMenuInfo, SetMenuInfo function [Menus and Other Resources], _win32_SetMenuInfo, _win32_setmenuinfo_cpp, menurc.setmenuinfo, winui._win32_setmenuinfo, winuser/SetMenuInfo
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
 - SetMenuInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetMenuInfo function


## -description


Sets information for a specified menu.


## -parameters




### -param

TBD




#### - [in]

Type: <b>HMENU</b>

A handle to a menu. 


#### - lpcmi [in]

Type: <b>LPCMENUINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms647575(v=VS.85).aspx">MENUINFO</a> structure for the menu. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>
 

 

