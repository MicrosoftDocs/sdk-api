---
UID: NF:winuser.AdjustWindowRectEx
title: AdjustWindowRectEx function
author: windows-sdk-content
description: Calculates the required size of the window rectangle, based on the desired size of the client rectangle. The window rectangle can then be passed to the CreateWindowEx function to create a window whose client area is the desired size.
old-location: winmsg\adjustwindowrectex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\adjustwindowrectex.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: AdjustWindowRectEx, AdjustWindowRectEx function [Windows and Messages], _win32_AdjustWindowRectEx, _win32_adjustwindowrectex_cpp, winmsg.adjustwindowrectex, winui._win32_adjustwindowrectex, winuser/AdjustWindowRectEx
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - AdjustWindowRectEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AdjustWindowRectEx function


## -description


Calculates the required size of the window rectangle, based on the desired size of the client rectangle. The window rectangle can then be passed to the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function to create a window whose client area is the desired size.


## -parameters




### -param lpRect [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the coordinates of the top-left and bottom-right corners of the desired client area. When the function returns, the structure contains the coordinates of the top-left and bottom-right corners of the window to accommodate the desired client area. 


### -param dwStyle [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">window style</a> of the window whose required size is to be calculated. Note that you cannot specify the <b>WS_OVERLAPPED</b> style. 


### -param bMenu [in]

Type: <b>BOOL</b>

Indicates whether the window has a menu. 


### -param dwExStyle [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/5830B16E-CD52-4a1a-A1BD-3AFE66BA5FDD">extended window style</a> of the window whose required size is to be calculated. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



A client rectangle is the smallest rectangle that completely encloses a client area. A window rectangle is the smallest rectangle that completely encloses the window, which includes the client area and the nonclient area. 

The <b>AdjustWindowRectEx</b> function does not add extra space when a menu bar wraps to two or more rows. 

The <b>AdjustWindowRectEx</b> function does not take the <b>WS_VSCROLL</b> or <b>WS_HSCROLL</b> styles into account. To account for the scroll bars, call the <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function with <b>SM_CXVSCROLL</b> or <b>SM_CYHSCROLL</b>. 

This API is not DPI aware, and should not be used if the calling thread is per-monitor DPI aware. For the DPI-aware version of this API, see <a href="https://msdn.microsoft.com/C7126165-1D64-4C04-9B8D-4F90AC2F2C67">AdjustWindowsRectExForDPI</a>. For more information on DPI awareness, see <a href="https://msdn.microsoft.com/6C419EEF-D898-4B50-8D16-E65A594487AA">the Windows High DPI documentation.</a>





## -see-also




<a href="https://msdn.microsoft.com/C7126165-1D64-4C04-9B8D-4F90AC2F2C67">AdjustWindowsRectExForDPI</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

