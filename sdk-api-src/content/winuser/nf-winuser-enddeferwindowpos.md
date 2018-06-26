---
UID: NF:winuser.EndDeferWindowPos
title: EndDeferWindowPos function
author: windows-sdk-content
description: Simultaneously updates the position and size of one or more windows in a single screen-refreshing cycle.
old-location: winmsg\enddeferwindowpos.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\enddeferwindowpos.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: EndDeferWindowPos, EndDeferWindowPos function [Windows and Messages], _win32_EndDeferWindowPos, _win32_enddeferwindowpos_cpp, winmsg.enddeferwindowpos, winui._win32_enddeferwindowpos, winuser/EndDeferWindowPos
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
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - EndDeferWindowPos
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EndDeferWindowPos function


## -description


Simultaneously updates the position and size of one or more windows in a single screen-refreshing cycle. 


## -parameters




### -param hWinPosInfo [in]

Type: <b>HDWP</b>

A handle to a multiple-window 
					– position structure that contains size and position information for one or more windows. This internal structure is returned by the <a href="https://msdn.microsoft.com/7df4ebad-c982-4b9c-8895-52f7ca0bf7e5">BeginDeferWindowPos</a> function or by the most recent call to the <a href="https://msdn.microsoft.com/2758de7b-c218-4a9b-b11b-b189301f7514">DeferWindowPos</a> function. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>EndDeferWindowPos</b> function sends the <a href="https://msdn.microsoft.com/45ecd966-5222-4738-9e99-8a6edbdd435a">WM_WINDOWPOSCHANGING</a> and <a href="https://msdn.microsoft.com/1eabd0b1-1f92-4576-b7fb-8af50fb04526">WM_WINDOWPOSCHANGED</a> messages to each window identified in the internal structure. 




## -see-also




<a href="https://msdn.microsoft.com/7df4ebad-c982-4b9c-8895-52f7ca0bf7e5">BeginDeferWindowPos</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/2758de7b-c218-4a9b-b11b-b189301f7514">DeferWindowPos</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/1eabd0b1-1f92-4576-b7fb-8af50fb04526">WM_WINDOWPOSCHANGED</a>



<a href="https://msdn.microsoft.com/45ecd966-5222-4738-9e99-8a6edbdd435a">WM_WINDOWPOSCHANGING</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

