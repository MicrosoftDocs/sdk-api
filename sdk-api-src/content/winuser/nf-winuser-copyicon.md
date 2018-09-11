---
UID: NF:winuser.CopyIcon
title: CopyIcon function
author: windows-sdk-content
description: Copies the specified icon from another module to the current module.
old-location: menurc\copyicon.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\copyicon.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CopyIcon, CopyIcon function [Menus and Other Resources], _win32_CopyIcon, _win32_copyicon_cpp, menurc.copyicon, winui._win32_copyicon, winuser/CopyIcon
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
 - CopyIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CopyIcon function


## -description


Copies the specified icon from another module to the current module.


## -parameters




### -param hIcon [in]

Type: <b>HICON</b>

A handle to the icon to be copied.


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the duplicate icon.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>CopyIcon</b> function enables an application or DLL to get its own handle to an icon owned by another module. If the other module is freed, the application icon will still be able to use the icon. 

Before closing, an application must call the <a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a> function to free any system resources associated with the icon.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648384(v=VS.85).aspx">CopyCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648064(v=VS.85).aspx">DrawIcon</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648065(v=VS.85).aspx">DrawIconEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646973(v=VS.85).aspx">Icons</a>



<b>Reference</b>
 

 

