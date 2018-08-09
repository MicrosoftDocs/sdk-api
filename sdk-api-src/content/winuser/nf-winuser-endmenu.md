---
UID: NF:winuser.EndMenu
title: EndMenu function
author: windows-sdk-content
description: Ends the calling thread's active menu.
old-location: menurc\endmenu.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\endmenu.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EndMenu, EndMenu function [Menus and Other Resources], _win32_EndMenu, _win32_endmenu_cpp, menurc.endmenu, winui._win32_endmenu, winuser/EndMenu
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
 - EndMenu
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EndMenu function


## -description


Ends the calling thread's active menu.


## -parameters






## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If a platform does not support <b>EndMenu</b>, send the owner of the active menu a <a href="https://msdn.microsoft.com/en-us/library/ms632615(v=VS.85).aspx">WM_CANCELMODE</a> message.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632615(v=VS.85).aspx">WM_CANCELMODE</a>
 

 

