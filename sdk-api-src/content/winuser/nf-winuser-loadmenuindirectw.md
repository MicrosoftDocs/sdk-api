---
UID: NF:winuser.LoadMenuIndirectW
title: LoadMenuIndirectW function
author: windows-sdk-content
description: Loads the specified menu template in memory.
old-location: menurc\loadmenuindirect.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\loadmenuindirect.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
api_name:
-	LoadMenuIndirect
-	LoadMenuIndirectA
-	LoadMenuIndirectW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LoadMenuIndirectW function


## -description


Loads the specified menu template in memory. 


## -parameters




### -param lpMenuTemplate [in]

Type: <b>const MENUTEMPLATE*</b>

A pointer to a menu template or an extended menu template. A menu template consists of a <a href="https://msdn.microsoft.com/7dd21370-9e26-4086-9ba1-98e79966c336">MENUITEMTEMPLATEHEADER</a> structure followed by one or more contiguous <a href="https://msdn.microsoft.com/9329aee3-83be-4409-98f4-e135f39c0f01">MENUITEMTEMPLATE</a> structures. An extended menu template consists of a <a href="https://msdn.microsoft.com/df763349-7127-482e-8613-74e68addde5d">MENUEX_TEMPLATE_HEADER</a> structure followed by one or more contiguous <a href="https://msdn.microsoft.com/f6e2fd0a-16b8-48e3-8597-341085a7adbd">MENUEX_TEMPLATE_ITEM</a> structures. 


## -returns



Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the menu.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



For both the ANSI and the Unicode version of this function, the strings in the <a href="https://msdn.microsoft.com/9329aee3-83be-4409-98f4-e135f39c0f01">MENUITEMTEMPLATE</a> structure must be Unicode strings. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/806297e1-0ee4-4471-a98a-598c1b48c0de">LoadMenu</a>



<a href="https://msdn.microsoft.com/df763349-7127-482e-8613-74e68addde5d">MENUEX_TEMPLATE_HEADER</a>



<a href="https://msdn.microsoft.com/f6e2fd0a-16b8-48e3-8597-341085a7adbd">MENUEX_TEMPLATE_ITEM</a>



<a href="https://msdn.microsoft.com/9329aee3-83be-4409-98f4-e135f39c0f01">MENUITEMTEMPLATE</a>



<a href="https://msdn.microsoft.com/7dd21370-9e26-4086-9ba1-98e79966c336">MENUITEMTEMPLATEHEADER</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

