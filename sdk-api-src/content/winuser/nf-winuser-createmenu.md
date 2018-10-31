---
UID: NF:winuser.CreateMenu
title: CreateMenu function
author: windows-sdk-content
description: Creates a menu. The menu is initially empty, but it can be filled with menu items by using the InsertMenuItem, AppendMenu, and InsertMenu functions.
old-location: menurc\createmenu.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\createmenu.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateMenu, CreateMenu function [Menus and Other Resources], _win32_CreateMenu, _win32_createmenu_cpp, menurc.createmenu, winui._win32_createmenu, winuser/CreateMenu
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
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - CreateMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateMenu function


## -description


Creates a menu. The menu is initially empty, but it can be filled with menu items by using the <a href="https://msdn.microsoft.com/be3819c2-8bdc-4a90-a188-ff8b4060eb8f">InsertMenuItem</a>, <a href="https://msdn.microsoft.com/07da4d45-a816-40c1-a5c5-c7fbe954be57">AppendMenu</a>, and <a href="https://msdn.microsoft.com/8ca7510a-e035-4ba2-98dd-57d777cae814">InsertMenu</a> functions. 


## -parameters






## -returns



Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the newly created menu.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Resources associated with a menu that is assigned to a window are freed automatically. If the menu is not assigned to a window, an application must free system resources associated with the menu before closing. An application frees menu resources by calling the <a href="https://msdn.microsoft.com/4fc9e332-09a6-4877-a831-e1128144530d">DestroyMenu</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/07da4d45-a816-40c1-a5c5-c7fbe954be57">AppendMenu</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b1341fe7-1532-4e0b-82f3-540cc88c0aa7">CreatePopupMenu</a>



<a href="https://msdn.microsoft.com/4fc9e332-09a6-4877-a831-e1128144530d">DestroyMenu</a>



<a href="https://msdn.microsoft.com/8ca7510a-e035-4ba2-98dd-57d777cae814">InsertMenu</a>



<a href="https://msdn.microsoft.com/be3819c2-8bdc-4a90-a188-ff8b4060eb8f">InsertMenuItem</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/86d61b87-99ad-45e1-bcff-af892b4bb51b">SetMenu</a>
 

 

