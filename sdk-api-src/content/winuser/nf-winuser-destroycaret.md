---
UID: NF:winuser.DestroyCaret
title: DestroyCaret function
author: windows-sdk-content
description: Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen.
old-location: menurc\destroycaret.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\destroycaret.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DestroyCaret, DestroyCaret function [Menus and Other Resources], _win32_DestroyCaret, _win32_destroycaret_cpp, menurc.destroycaret, winui._win32_destroycaret, winuser/DestroyCaret
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
 - DestroyCaret
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DestroyCaret function


## -description


Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen. 


## -parameters






## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>DestroyCaret</b> destroys the caret only if a window in the current task owns the caret. If a window that is not in the current task owns the caret, <b>DestroyCaret</b> does nothing and returns <b>FALSE</b>. 

The system provides one caret per queue. A window should create a caret only when it has the keyboard focus or is active. The window should destroy the caret before losing the keyboard focus or becoming inactive. 

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms648398(v=VS.85).aspx">Destroying a Caret</a>




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646968(v=VS.85).aspx">Carets</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648399(v=VS.85).aspx">CreateCaret</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648403(v=VS.85).aspx">HideCaret</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648406(v=VS.85).aspx">ShowCaret</a>
 

 

