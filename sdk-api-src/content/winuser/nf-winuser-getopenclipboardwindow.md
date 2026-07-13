---
UID: NF:winuser.GetOpenClipboardWindow
title: GetOpenClipboardWindow function (winuser.h)
description: Retrieves the handle to the window that currently has the clipboard open.
helpviewer_keywords: ["GetOpenClipboardWindow","GetOpenClipboardWindow function [Data Exchange]","_win32_GetOpenClipboardWindow","_win32_getopenclipboardwindow_cpp","dataxchg.getopenclipboardwindow","winui._win32_getopenclipboardwindow","winuser/GetOpenClipboardWindow"]
old-location: dataxchg\getopenclipboardwindow.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardfunctions\getopenclipboardwindow.htm
ms.date: 12/05/2018
ms.keywords: GetOpenClipboardWindow, GetOpenClipboardWindow function [Data Exchange], _win32_GetOpenClipboardWindow, _win32_getopenclipboardwindow_cpp, dataxchg.getopenclipboardwindow, winui._win32_getopenclipboardwindow, winuser/GetOpenClipboardWindow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetOpenClipboardWindow
 - winuser/GetOpenClipboardWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - User32.dll
api_name:
 - GetOpenClipboardWindow
---

# GetOpenClipboardWindow function


## -description

Retrieves the handle to the window that currently has the clipboard open.



## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the window that has the clipboard open. If no window has the clipboard open, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If an application or DLL specifies a <b>NULL</b> window handle when calling the <a href="/windows/desktop/api/winuser/nf-winuser-openclipboard">OpenClipboard</a> function, the clipboard is opened but is not associated with a window. In such a case, <b>GetOpenClipboardWindow</b> returns <b>NULL</b>.

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getclipboardowner">GetClipboardOwner</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclipboardviewer">GetClipboardViewer</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openclipboard">OpenClipboard</a>



<b>Reference</b>
