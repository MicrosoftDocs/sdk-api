---
UID: NF:winuser.LoadMenuIndirectA
title: LoadMenuIndirectA function (winuser.h)
description: Loads the specified menu template in memory.
old-location: menurc\loadmenuindirect.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\loadmenuindirect.htm
ms.date: 12/05/2018
ms.keywords: LoadMenuIndirect, LoadMenuIndirect function [Menus and Other Resources], LoadMenuIndirectA, LoadMenuIndirectW, _win32_LoadMenuIndirect, _win32_loadmenuindirect_cpp, menurc.loadmenuindirect, winui._win32_loadmenuindirect, winuser/LoadMenuIndirect, winuser/LoadMenuIndirectA, winuser/LoadMenuIndirectW
ms.topic: function
f1_keywords:
- winuser/LoadMenuIndirect
dev_langs:
- c++
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
- LoadMenuIndirect
- LoadMenuIndirectA
- LoadMenuIndirectW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LoadMenuIndirectA function


## -description


Loads the specified menu template in memory. 


## -parameters




### -param lpMenuTemplate [in]

Type: <b>const MENUTEMPLATE*</b>

A pointer to a menu template or an extended menu template. A menu template consists of a <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-menuitemtemplateheader">MENUITEMTEMPLATEHEADER</a> structure followed by one or more contiguous <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-menuitemtemplate">MENUITEMTEMPLATE</a> structures. An extended menu template consists of a <a href="https://docs.microsoft.com/windows/desktop/menurc/menuex-template-header">MENUEX_TEMPLATE_HEADER</a> structure followed by one or more contiguous <a href="https://docs.microsoft.com/windows/desktop/menurc/menuex-template-item">MENUEX_TEMPLATE_ITEM</a> structures. 


## -returns



Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the menu.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



For both the ANSI and the Unicode version of this function, the strings in the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-menuitemtemplate">MENUITEMTEMPLATE</a> structure must be Unicode strings. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadmenua">LoadMenu</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/menuex-template-header">MENUEX_TEMPLATE_HEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/menuex-template-item">MENUEX_TEMPLATE_ITEM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-menuitemtemplate">MENUITEMTEMPLATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-menuitemtemplateheader">MENUITEMTEMPLATEHEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
 

 

