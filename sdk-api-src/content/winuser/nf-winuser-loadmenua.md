---
UID: NF:winuser.LoadMenuA
title: LoadMenuA function
author: windows-sdk-content
description: Loads the specified menu resource from the executable (.exe) file associated with an application instance.
old-location: menurc\loadmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\loadmenu.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: LoadMenu, LoadMenu function [Menus and Other Resources], LoadMenuA, LoadMenuW, _win32_LoadMenu, _win32_loadmenu_cpp, menurc.loadmenu, winui._win32_loadmenu, winuser/LoadMenu, winuser/LoadMenuA, winuser/LoadMenuW
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
req.unicode-ansi: LoadMenuW (Unicode) and LoadMenuA (ANSI)
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
 - LoadMenu
 - LoadMenuA
 - LoadMenuW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- LoadMenuA
: 
---

# LoadMenuA function


## -description


Loads the specified menu resource from the executable (.exe) file associated with an application instance. 


## -parameters




### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module containing the menu resource to be loaded. 


### -param lpMenuName [in]

Type: <b>LPCTSTR</b>

The name of the menu resource. Alternatively, this parameter can consist of the resource identifier in the low-order word and zero in the high-order word. To create this value, use the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro. 


## -returns



Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the menu resource.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <a href="https://msdn.microsoft.com/4fc9e332-09a6-4877-a831-e1128144530d">DestroyMenu</a> function is used, before an application closes, to destroy the menu and free memory that the loaded menu occupied. 


#### Examples

For an example, see <a href="using_menus.htm">Displaying a Shortcut Menu</a>

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/01736486-6dee-43fe-80a7-06c4cf13a23e">LoadMenuIndirect</a>



<a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

