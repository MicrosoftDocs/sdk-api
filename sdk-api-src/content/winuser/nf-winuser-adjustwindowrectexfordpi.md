---
UID: NF:winuser.AdjustWindowRectExForDpi
title: AdjustWindowRectExForDpi function
author: windows-sdk-content
description: Calculates the required size of the window rectangle, based on the desired size of the client rectangle and the provided DPI.
old-location: hidpi\adjustwindowrectexfordpi.htm
tech.root: hidpi
ms.assetid: C7126165-1D64-4C04-9B8D-4F90AC2F2C67
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: AdjustWindowRectExForDpi, AdjustWindowRectExForDpi function [High DPI], hidpi.adjustwindowrectexfordpi, winuser/AdjustWindowRectExForDpi
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - AdjustWindowRectExForDpi
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AdjustWindowRectExForDpi function


## -description


Calculates the required size of the window rectangle, based on the desired size of the client rectangle and the provided DPI. This window rectangle can then be passed to the <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> function to create a window with a client area of the desired size.


## -parameters




### -param lpRect [in, out]

A pointer to a <b>RECT</b> structure that contains the coordinates of the top-left and bottom-right corners of the desired client area. When the function returns, the structure contains the coordinates of the top-left and bottom-right corners of the window to accommodate the desired client area. 


### -param dwStyle [in]

The <a href="https://msdn.microsoft.com/en-us/library/ms632600(v=VS.85).aspx">Window Style</a> of the window whose required size is to be calculated. Note that you cannot specify the <b>WS_OVERLAPPED</b> style. 


### -param bMenu [in]

Indicates whether the window has a menu.


### -param dwExStyle [in]

The <a href="https://msdn.microsoft.com/5830B16E-CD52-4a1a-A1BD-3AFE66BA5FDD">Extended Window Style</a> of the window whose required size is to be calculated. 


### -param dpi [in]

The DPI to use for scaling.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



This function returns the same result as <a href="https://msdn.microsoft.com/en-us/library/ms632667(v=VS.85).aspx">AdjustWindowRectEx</a> but scales it according to an arbitrary DPI you provide if appropriate.



