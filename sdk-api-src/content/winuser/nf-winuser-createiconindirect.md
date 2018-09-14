---
UID: NF:winuser.CreateIconIndirect
title: CreateIconIndirect function
author: windows-sdk-content
description: Creates an icon or cursor from an ICONINFO structure.
old-location: menurc\createiconindirect.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\createiconindirect.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateIconIndirect, CreateIconIndirect function [Menus and Other Resources], _win32_CreateIconIndirect, _win32_createiconindirect_cpp, menurc.createiconindirect, winui._win32_createiconindirect, winuser/CreateIconIndirect
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
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - CreateIconIndirect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateIconIndirect function


## -description


Creates an icon or cursor from an <a href="https://msdn.microsoft.com/55559fac-b561-4fd0-98e6-bbb6fc610033">ICONINFO</a> structure.


## -parameters




### -param piconinfo [in]

Type: <b>PICONINFO</b>

A pointer to an <a href="https://msdn.microsoft.com/55559fac-b561-4fd0-98e6-bbb6fc610033">ICONINFO</a> structure the function uses to create the icon or cursor. 


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the icon or cursor that is created.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The system copies the bitmaps in the <a href="https://msdn.microsoft.com/55559fac-b561-4fd0-98e6-bbb6fc610033">ICONINFO</a> structure before creating the icon or cursor. Because the system may temporarily select the bitmaps in a device context, the <b>hbmMask</b> and <b>hbmColor</b> members of the <b>ICONINFO</b> structure should not already be selected into a device context. The application must continue to manage the original bitmaps and delete them when they are no longer necessary. 

When you are finished using the icon, destroy it using the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>



<a href="https://msdn.microsoft.com/55559fac-b561-4fd0-98e6-bbb6fc610033">ICONINFO</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

