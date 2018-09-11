---
UID: NF:winuser.LoadMenuA
title: LoadMenuA function
author: windows-sdk-content
description: Loads the specified menu resource from the executable (.exe) file associated with an application instance.
old-location: menurc\loadmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\loadmenu.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
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

The name of the menu resource. Alternatively, this parameter can consist of the resource identifier in the low-order word and zero in the high-order word. To create this value, use the <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a> macro. 


## -returns



Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the menu resource.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/ms647631(v=VS.85).aspx">DestroyMenu</a> function is used, before an application closes, to destroy the menu and free memory that the loaded menu occupied. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms647558(v=VS.85).aspx">Displaying a Shortcut Menu</a>

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647991(v=VS.85).aspx">LoadMenuIndirect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>
 

 

