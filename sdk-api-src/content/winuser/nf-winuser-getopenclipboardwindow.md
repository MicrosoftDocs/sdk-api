---
UID: NF:winuser.GetOpenClipboardWindow
title: GetOpenClipboardWindow function
author: windows-sdk-content
description: Retrieves the handle to the window that currently has the clipboard open.
old-location: dataxchg\getopenclipboardwindow.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getopenclipboardwindow.htm
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetOpenClipboardWindow, GetOpenClipboardWindow function [Data Exchange], _win32_GetOpenClipboardWindow, _win32_getopenclipboardwindow_cpp, dataxchg.getopenclipboardwindow, winui._win32_getopenclipboardwindow, winuser/GetOpenClipboardWindow
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
api_name:
 - GetOpenClipboardWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetOpenClipboardWindow function


## -description


Retrieves the handle to the window that currently has the clipboard open. 


## -parameters






## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the window that has the clipboard open. If no window has the clipboard open, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If an application or DLL specifies a <b>NULL</b> window handle when calling the <a href="https://msdn.microsoft.com/494e4e6f-6d82-45cc-8c0b-f8c54056bc5f">OpenClipboard</a> function, the clipboard is opened but is not associated with a window. In such a case, <b>GetOpenClipboardWindow</b> returns <b>NULL</b>. 




## -see-also




<a href="https://msdn.microsoft.com/61a9bff7-3c46-4e42-81f7-e020ff0b667f">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/96c06602-05ec-4f38-a53b-1729f2c1ce4f">GetClipboardOwner</a>



<a href="https://msdn.microsoft.com/700bee1f-1bed-4fc8-a4ce-7a48bd05e90b">GetClipboardViewer</a>



<a href="https://msdn.microsoft.com/494e4e6f-6d82-45cc-8c0b-f8c54056bc5f">OpenClipboard</a>



<b>Reference</b>
 

 

