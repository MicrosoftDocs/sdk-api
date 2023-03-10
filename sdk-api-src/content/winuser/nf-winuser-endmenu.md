---
UID: NF:winuser.EndMenu
title: EndMenu function (winuser.h)
description: Ends the calling thread's active menu.
helpviewer_keywords: ["EndMenu","EndMenu function [Menus and Other Resources]","_win32_EndMenu","_win32_endmenu_cpp","menurc.endmenu","winui._win32_endmenu","winuser/EndMenu"]
old-location: menurc\endmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\endmenu.htm
ms.date: 12/05/2018
ms.keywords: EndMenu, EndMenu function [Menus and Other Resources], _win32_EndMenu, _win32_endmenu_cpp, menurc.endmenu, winui._win32_endmenu, winuser/EndMenu
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EndMenu
 - winuser/EndMenu
dev_langs:
 - c++
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
req.apiset: ext-ms-win-ntuser-menu-l1-1-0 (introduced in Windows 8)
---

# EndMenu function


## -description

Ends the calling thread's active menu.



## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a platform does not support <b>EndMenu</b>, send the owner of the active menu a <a href="/windows/desktop/winmsg/wm-cancelmode">WM_CANCELMODE</a> message.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-cancelmode">WM_CANCELMODE</a>
