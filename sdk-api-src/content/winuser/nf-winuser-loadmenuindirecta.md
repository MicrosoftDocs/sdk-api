---
UID: NF:winuser.LoadMenuIndirectA
title: LoadMenuIndirectA function
author: windows-sdk-content
description: Loads the specified menu template in memory.
old-location: menurc\loadmenuindirect.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\loadmenuindirect.htm
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: LoadMenuIndirect, LoadMenuIndirect function [Menus and Other Resources], LoadMenuIndirectA, LoadMenuIndirectW, _win32_LoadMenuIndirect, _win32_loadmenuindirect_cpp, menurc.loadmenuindirect, winui._win32_loadmenuindirect, winuser/LoadMenuIndirect, winuser/LoadMenuIndirectA, winuser/LoadMenuIndirectW
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
req.unicode-ansi: LoadMenuIndirectW (Unicode) and LoadMenuIndirectA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - LoadMenuIndirect
 - LoadMenuIndirectA
 - LoadMenuIndirectW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LoadMenuIndirectA function


## -description


Loads the specified menu template in memory. 


## -parameters




### -param lpMenuTemplate [in]

Type: <b>const MENUTEMPLATE*</b>

A pointer to a menu template or an extended menu template. A menu template consists of a <a href="https://msdn.microsoft.com/library/ms647583(v=VS.85).aspx">MENUITEMTEMPLATEHEADER</a> structure followed by one or more contiguous <a href="https://msdn.microsoft.com/library/ms647581(v=VS.85).aspx">MENUITEMTEMPLATE</a> structures. An extended menu template consists of a <a href="https://msdn.microsoft.com/library/ms647567(v=VS.85).aspx">MENUEX_TEMPLATE_HEADER</a> structure followed by one or more contiguous <a href="https://msdn.microsoft.com/library/ms647569(v=VS.85).aspx">MENUEX_TEMPLATE_ITEM</a> structures. 


## -returns



Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the menu.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



For both the ANSI and the Unicode version of this function, the strings in the <a href="https://msdn.microsoft.com/library/ms647581(v=VS.85).aspx">MENUITEMTEMPLATE</a> structure must be Unicode strings. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms647990(v=VS.85).aspx">LoadMenu</a>



<a href="https://msdn.microsoft.com/library/ms647567(v=VS.85).aspx">MENUEX_TEMPLATE_HEADER</a>



<a href="https://msdn.microsoft.com/library/ms647569(v=VS.85).aspx">MENUEX_TEMPLATE_ITEM</a>



<a href="https://msdn.microsoft.com/library/ms647581(v=VS.85).aspx">MENUITEMTEMPLATE</a>



<a href="https://msdn.microsoft.com/library/ms647583(v=VS.85).aspx">MENUITEMTEMPLATEHEADER</a>



<a href="https://msdn.microsoft.com/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>
 

 

