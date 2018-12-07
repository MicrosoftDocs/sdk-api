---
UID: NF:winuser.SetCaretBlinkTime
title: SetCaretBlinkTime function
author: windows-sdk-content
description: Sets the caret blink time to the specified number of milliseconds. The blink time is the elapsed time, in milliseconds, required to invert the caret's pixels.
old-location: menurc\setcaretblinktime.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\setcaretblinktime.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetCaretBlinkTime, SetCaretBlinkTime function [Menus and Other Resources], _win32_SetCaretBlinkTime, _win32_setcaretblinktime_cpp, menurc.setcaretblinktime, winui._win32_setcaretblinktime, winuser/SetCaretBlinkTime
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
 - Ext-MS-Win-NTUser-caret-l1-1-0.dll
 - api-ms-win-ntuser-ie-caret-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - SetCaretBlinkTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetCaretBlinkTime function


## -description


Sets the caret blink time to the specified number of milliseconds. The blink time is the elapsed time, in milliseconds, required to invert the caret's pixels. 


## -parameters




### -param uMSeconds [in]

Type: <b>UINT</b>

The new blink time, in milliseconds. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The user can set the blink time using the Control Panel. Applications should respect the setting that the user has chosen. The <b>SetCaretBlinkTime</b> function should only be used by application that allow the user to set the blink time, such as a Control Panel applet.

If you change the blink time, subsequently activated applications will use the modified blink time, even if you restore the previous blink time when you lose the keyboard focus or become inactive. This is due to the multithreaded environment, where deactivation of your application is not synchronized with the activation of another application. This feature allows the system to activate another application even if the current application is not responding. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646968(v=VS.85).aspx">Carets</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648401(v=VS.85).aspx">GetCaretBlinkTime</a>



<b>Reference</b>
 

 

