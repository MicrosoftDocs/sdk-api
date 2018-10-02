---
UID: NF:winuser.GetOpenClipboardWindow
title: GetOpenClipboardWindow function
author: windows-sdk-content
description: Retrieves the handle to the window that currently has the clipboard open.
old-location: dataxchg\getopenclipboardwindow.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getopenclipboardwindow.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetOpenClipboardWindow, GetOpenClipboardWindow function [Data Exchange], _win32_GetOpenClipboardWindow, _win32_getopenclipboardwindow_cpp, dataxchg.getopenclipboardwindow, winui._win32_getopenclipboardwindow, winuser/GetOpenClipboardWindow
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
api_name:
 - GetOpenClipboardWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetOpenClipboardWindow function


## -description


Retrieves the handle to the window that currently has the clipboard open. 


## -parameters






## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the window that has the clipboard open. If no window has the clipboard open, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If an application or DLL specifies a <b>NULL</b> window handle when calling the <a href="https://msdn.microsoft.com/en-us/library/ms649048(v=VS.85).aspx">OpenClipboard</a> function, the clipboard is opened but is not associated with a window. In such a case, <b>GetOpenClipboardWindow</b> returns <b>NULL</b>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648709(v=VS.85).aspx">Clipboard</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms649041(v=VS.85).aspx">GetClipboardOwner</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649043(v=VS.85).aspx">GetClipboardViewer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649048(v=VS.85).aspx">OpenClipboard</a>



<b>Reference</b>
 

 

