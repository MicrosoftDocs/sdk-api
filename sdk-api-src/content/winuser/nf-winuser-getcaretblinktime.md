---
UID: NF:winuser.GetCaretBlinkTime
title: GetCaretBlinkTime function
author: windows-sdk-content
description: Retrieves the time required to invert the caret's pixels. The user can set this value.
old-location: menurc\getcaretblinktime.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\getcaretblinktime.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCaretBlinkTime, GetCaretBlinkTime function [Menus and Other Resources], _win32_GetCaretBlinkTime, _win32_getcaretblinktime_cpp, menurc.getcaretblinktime, winui._win32_getcaretblinktime, winuser/GetCaretBlinkTime
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
 - GetCaretBlinkTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetCaretBlinkTime
: 
---

# GetCaretBlinkTime function


## -description


Retrieves the time required to invert the caret's pixels.
          The user can set this value. 


## -parameters






## -returns



Type: <b>UINT</b>

If the function succeeds, the return value is the blink time, in milliseconds.
          

A return value of <b>INFINITE</b> indicates that the caret does not blink.

A return value is zero indicates that the function has failed.
             To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646968(v=VS.85).aspx">Carets</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648404(v=VS.85).aspx">SetCaretBlinkTime</a>
 

 

