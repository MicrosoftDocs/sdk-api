---
UID: NF:winuser.KillTimer
title: KillTimer function
author: windows-sdk-content
description: Destroys the specified timer.
old-location: winmsg\killtimer.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\timers\timerreference\timerfunctions\killtimer.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: KillTimer, KillTimer function [Windows and Messages], _win32_KillTimer, _win32_killtimer_cpp, winmsg.killtimer, winui._win32_killtimer, winuser/KillTimer
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
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - KillTimer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# KillTimer function


## -description


Destroys the specified timer. 


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window associated with the specified timer. This value must be the same as the 
					<i>hWnd</i> value passed to the <a href="https://msdn.microsoft.com/393038fa-972f-4151-b90a-cebf84c50867">SetTimer</a> function that created the timer. 


### -param uIDEvent [in]

Type: <b>UINT_PTR</b>

The timer to be destroyed. If the window handle passed to <a href="https://msdn.microsoft.com/393038fa-972f-4151-b90a-cebf84c50867">SetTimer</a> is valid, this parameter must be the same as the
					<i>nIDEvent</i> 

value passed to <b>SetTimer</b>. If the application calls <b>SetTimer</b> with 
					<i>hWnd</i> set to <b>NULL</b>, this parameter must be the timer identifier returned by <b>SetTimer</b>. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>KillTimer</b> function does not remove <a href="https://msdn.microsoft.com/419e3f05-35ec-4e48-b24d-ab98df687b20">WM_TIMER</a> messages already posted to the message queue.


#### Examples

For an example, see <a href="using_timers.htm">Destroying a Timer</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/393038fa-972f-4151-b90a-cebf84c50867">SetTimer</a>



<a href="https://msdn.microsoft.com/be335927-a78d-4023-bedb-94aaf3a561ae">Timers</a>



<a href="https://msdn.microsoft.com/419e3f05-35ec-4e48-b24d-ab98df687b20">WM_TIMER</a>
 

 

