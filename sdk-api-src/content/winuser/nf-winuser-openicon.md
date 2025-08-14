---
UID: NF:winuser.OpenIcon
title: OpenIcon function (winuser.h)
description: Restores a minimized (iconic) window to its previous size and position; it then activates the window.
helpviewer_keywords: ["OpenIcon","OpenIcon function [Windows and Messages]","_win32_OpenIcon","_win32_openicon_cpp","winmsg.openicon","winui._win32_openicon","winuser/OpenIcon"]
old-location: winmsg\openicon.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\openicon.htm
ms.date: 12/05/2018
ms.keywords: OpenIcon, OpenIcon function [Windows and Messages], _win32_OpenIcon, _win32_openicon_cpp, winmsg.openicon, winui._win32_openicon, winuser/OpenIcon
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
 - OpenIcon
 - winuser/OpenIcon
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - ext-ms-win-ntuser-window-l1-1-4.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - ext-ms-win-ntuser-window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-0.dll
 - User32.dll
api_name:
 - OpenIcon
---

# OpenIcon function


## -description

Restores a minimized (iconic) window to its previous size and position; it then activates the window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be restored and activated.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>OpenIcon</b> sends a <a href="/windows/desktop/winmsg/wm-queryopen">WM_QUERYOPEN</a> message to the given window.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-closewindow">CloseWindow</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-isiconic">IsIconic</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>