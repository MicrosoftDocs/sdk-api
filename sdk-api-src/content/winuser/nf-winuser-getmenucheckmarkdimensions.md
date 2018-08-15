---
UID: NF:winuser.GetMenuCheckMarkDimensions
title: GetMenuCheckMarkDimensions function
author: windows-sdk-content
description: Retrieves the dimensions of the default check-mark bitmap.
old-location: menurc\getmenucheckmarkdimensions.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenucheckmarkdimensions.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMenuCheckMarkDimensions, GetMenuCheckMarkDimensions function [Menus and Other Resources], _win32_GetMenuCheckMarkDimensions, _win32_getmenucheckmarkdimensions_cpp, menurc.getmenucheckmarkdimensions, winui._win32_getmenucheckmarkdimensions, winuser/GetMenuCheckMarkDimensions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
api_name:
 - GetMenuCheckMarkDimensions
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetMenuCheckMarkDimensions function


## -description


Retrieves the dimensions of the default check-mark bitmap. The system displays this bitmap next to selected menu items. Before calling the <a href="https://msdn.microsoft.com/en-us/library/ms647998(v=VS.85).aspx">SetMenuItemBitmaps</a> function to replace the default check-mark bitmap for a menu item, an application must determine the correct bitmap size by calling <b>GetMenuCheckMarkDimensions</b>. 
<div class="alert"><b>Note</b>  The <b>GetMenuCheckMarkDimensions</b> function is included only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function with the <b>CXMENUCHECK</b> and <b>CYMENUCHECK</b> values to retrieve the bitmap dimensions.</div><div> </div>

## -parameters






## -returns



Type: <b>LONG</b>

The return value specifies the height and width, in pixels, of the default check-mark bitmap. The high-order word contains the height; the low-order word contains the width. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms647998(v=VS.85).aspx">SetMenuItemBitmaps</a>
 

 

