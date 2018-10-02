---
UID: NF:winuser.HideCaret
title: HideCaret function
author: windows-sdk-content
description: Removes the caret from the screen. Hiding a caret does not destroy its current shape or invalidate the insertion point.
old-location: menurc\hidecaret.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\hidecaret.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: HideCaret, HideCaret function [Menus and Other Resources], _win32_HideCaret, _win32_hidecaret_cpp, menurc.hidecaret, winui._win32_hidecaret, winuser/HideCaret
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
 - HideCaret
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HideCaret function


## -description


Removes the caret from the screen. Hiding a caret does not destroy its current shape or invalidate the insertion point. 


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window that owns the caret. If this parameter is <b>NULL</b>, <b>HideCaret</b> searches the current task for the window that owns the caret. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>HideCaret</b> hides the caret only if the specified window owns the caret. If the specified window does not own the caret, <b>HideCaret</b> does nothing and returns <b>FALSE</b>. 

Hiding is cumulative. If your application calls <b>HideCaret</b> five times in a row, it must also call <a href="https://msdn.microsoft.com/1a3a141e-9b5a-495a-8138-b9522933499f">ShowCaret</a> five times before the caret is displayed. 

For an example, see <a href="using_carets.htm">Hiding a Caret</a>.




## -see-also




<a href="https://msdn.microsoft.com/34ff3420-a1d2-46cc-9378-4b3340bec8c8">Carets</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f936c2cd-57a2-47ad-8be1-a2d99dcbe709">CreateCaret</a>



<a href="https://msdn.microsoft.com/ed434af6-1146-41b7-a4dc-8b5215a9ff43">DestroyCaret</a>



<a href="https://msdn.microsoft.com/14786dc7-bdd2-45e5-8073-b8dc3f5d30de">GetCaretPos</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0a8d4ca6-d409-4468-b29a-552adbea0918">SetCaretPos</a>



<a href="https://msdn.microsoft.com/1a3a141e-9b5a-495a-8138-b9522933499f">ShowCaret</a>
 

 

