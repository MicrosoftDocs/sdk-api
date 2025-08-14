---
UID: NF:winuser.LoadMenuIndirectW
title: LoadMenuIndirectW function (winuser.h)
description: Loads the specified menu template in memory. (Unicode)
helpviewer_keywords: ["LoadMenuIndirect", "LoadMenuIndirect function [Menus and Other Resources]", "LoadMenuIndirectW", "_win32_LoadMenuIndirect", "_win32_loadmenuindirect_cpp", "menurc.loadmenuindirect", "winui._win32_loadmenuindirect", "winuser/LoadMenuIndirect", "winuser/LoadMenuIndirectW"]
old-location: menurc\loadmenuindirect.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\loadmenuindirect.htm
ms.date: 12/05/2018
ms.keywords: LoadMenuIndirect, LoadMenuIndirect function [Menus and Other Resources], LoadMenuIndirectA, LoadMenuIndirectW, _win32_LoadMenuIndirect, _win32_loadmenuindirect_cpp, menurc.loadmenuindirect, winui._win32_loadmenuindirect, winuser/LoadMenuIndirect, winuser/LoadMenuIndirectA, winuser/LoadMenuIndirectW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LoadMenuIndirectW
 - winuser/LoadMenuIndirectW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-menu-l1-1-3.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - ext-ms-win-ntuser-menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-0.dll
 - User32.dll
api_name:
 - LoadMenuIndirect
 - LoadMenuIndirectA
 - LoadMenuIndirectW
---

# LoadMenuIndirectW function


## -description

Loads the specified menu template in memory.

## -parameters

### -param lpMenuTemplate [in]

Type: <b>const MENUTEMPLATE*</b>

A pointer to a menu template or an extended menu template. A menu template consists of a <a href="/windows/desktop/api/winuser/ns-winuser-menuitemtemplateheader">MENUITEMTEMPLATEHEADER</a> structure followed by one or more contiguous <a href="/windows/desktop/api/winuser/ns-winuser-menuitemtemplate">MENUITEMTEMPLATE</a> structures. An extended menu template consists of a <a href="/windows/desktop/menurc/menuex-template-header">MENUEX_TEMPLATE_HEADER</a> structure followed by one or more contiguous <a href="/windows/desktop/menurc/menuex-template-item">MENUEX_TEMPLATE_ITEM</a> structures.

## -returns

Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the menu.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For both the ANSI and the Unicode version of this function, the strings in the <a href="/windows/desktop/api/winuser/ns-winuser-menuitemtemplate">MENUITEMTEMPLATE</a> structure must be Unicode strings. 





> [!NOTE]
> The winuser.h header defines LoadMenuIndirect as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-loadmenua">LoadMenu</a>



<a href="/windows/desktop/menurc/menuex-template-header">MENUEX_TEMPLATE_HEADER</a>



<a href="/windows/desktop/menurc/menuex-template-item">MENUEX_TEMPLATE_ITEM</a>



<a href="/windows/desktop/api/winuser/ns-winuser-menuitemtemplate">MENUITEMTEMPLATE</a>



<a href="/windows/desktop/api/winuser/ns-winuser-menuitemtemplateheader">MENUITEMTEMPLATEHEADER</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>
