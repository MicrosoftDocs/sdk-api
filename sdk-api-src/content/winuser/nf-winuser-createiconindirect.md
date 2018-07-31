---
UID: NF:winuser.CreateIconIndirect
title: CreateIconIndirect function
author: windows-sdk-content
description: Creates an icon or cursor from an ICONINFO structure.
old-location: menurc\createiconindirect.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\createiconindirect.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CreateIconIndirect, CreateIconIndirect function [Menus and Other Resources], _win32_CreateIconIndirect, _win32_createiconindirect_cpp, menurc.createiconindirect, winui._win32_createiconindirect, winuser/CreateIconIndirect
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
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - CreateIconIndirect
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CreateIconIndirect function


## -description


Creates an icon or cursor from an <a href="https://msdn.microsoft.com/en-us/library/ms648052(v=VS.85).aspx">ICONINFO</a> structure.


## -parameters




### -param piconinfo [in]

Type: <b>PICONINFO</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms648052(v=VS.85).aspx">ICONINFO</a> structure the function uses to create the icon or cursor. 


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the icon or cursor that is created.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The system copies the bitmaps in the <a href="https://msdn.microsoft.com/en-us/library/ms648052(v=VS.85).aspx">ICONINFO</a> structure before creating the icon or cursor. Because the system may temporarily select the bitmaps in a device context, the <b>hbmMask</b> and <b>hbmColor</b> members of the <b>ICONINFO</b> structure should not already be selected into a device context. The application must continue to manage the original bitmaps and delete them when they are no longer necessary. 

When you are finished using the icon, destroy it using the <a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a> function.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648052(v=VS.85).aspx">ICONINFO</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646973(v=VS.85).aspx">Icons</a>



<b>Reference</b>
 

 

