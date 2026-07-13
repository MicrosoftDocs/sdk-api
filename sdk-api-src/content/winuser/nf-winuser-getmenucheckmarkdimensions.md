---
UID: NF:winuser.GetMenuCheckMarkDimensions
title: GetMenuCheckMarkDimensions function (winuser.h)
description: Retrieves the dimensions of the default check-mark bitmap.
helpviewer_keywords: ["GetMenuCheckMarkDimensions","GetMenuCheckMarkDimensions function [Menus and Other Resources]","_win32_GetMenuCheckMarkDimensions","_win32_getmenucheckmarkdimensions_cpp","menurc.getmenucheckmarkdimensions","winui._win32_getmenucheckmarkdimensions","winuser/GetMenuCheckMarkDimensions"]
old-location: menurc\getmenucheckmarkdimensions.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenucheckmarkdimensions.htm
ms.date: 12/05/2018
ms.keywords: GetMenuCheckMarkDimensions, GetMenuCheckMarkDimensions function [Menus and Other Resources], _win32_GetMenuCheckMarkDimensions, _win32_getmenucheckmarkdimensions_cpp, menurc.getmenucheckmarkdimensions, winui._win32_getmenucheckmarkdimensions, winuser/GetMenuCheckMarkDimensions
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
 - GetMenuCheckMarkDimensions
 - winuser/GetMenuCheckMarkDimensions
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
 - GetMenuCheckMarkDimensions
---

# GetMenuCheckMarkDimensions function


## -description

Retrieves the dimensions of the default check-mark bitmap. The system displays this bitmap next to selected menu items. Before calling the <a href="/windows/desktop/api/winuser/nf-winuser-setmenuitembitmaps">SetMenuItemBitmaps</a> function to replace the default check-mark bitmap for a menu item, an application must determine the correct bitmap size by calling <b>GetMenuCheckMarkDimensions</b>. 
<div class="alert"><b>Note</b>  The <b>GetMenuCheckMarkDimensions</b> function is included only for compatibility with 16-bit versions of Windows. Applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> function with the <b>CXMENUCHECK</b> and <b>CYMENUCHECK</b> values to retrieve the bitmap dimensions.</div><div> </div>



## -returns

Type: <b>LONG</b>

The return value specifies the height and width, in pixels, of the default check-mark bitmap. The high-order word contains the height; the low-order word contains the width.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setmenuitembitmaps">SetMenuItemBitmaps</a>
