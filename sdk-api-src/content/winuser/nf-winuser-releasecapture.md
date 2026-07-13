---
UID: NF:winuser.ReleaseCapture
title: ReleaseCapture function (winuser.h)
description: Releases the mouse capture from a window in the current thread and restores normal mouse input processing.
helpviewer_keywords: ["ReleaseCapture","ReleaseCapture function [Keyboard and Mouse Input]","_win32_ReleaseCapture","_win32_releasecapture_cpp","inputdev.releasecapture","winui._win32_releasecapture","winuser/ReleaseCapture"]
old-location: inputdev\releasecapture.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\releasecapture.htm
ms.date: 12/05/2018
ms.keywords: ReleaseCapture, ReleaseCapture function [Keyboard and Mouse Input], _win32_ReleaseCapture, _win32_releasecapture_cpp, inputdev.releasecapture, winui._win32_releasecapture, winuser/ReleaseCapture
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
 - ReleaseCapture
 - winuser/ReleaseCapture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-mouse-l1-1-0.dll
 - ext-ms-win-ntuser-mouse-l1-1-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-mouse-l1-1-0.dll
 - api-ms-win-ntuser-ie-mouse-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - ReleaseCapture
req.apiset: ext-ms-win-ntuser-mouse-l1-1-0 (introduced in Windows 8)
---

# ReleaseCapture function


## -description

Releases the mouse capture from a window in the current thread and restores normal mouse input processing. A window that has captured the mouse receives all mouse input, regardless of the position of the cursor, except when a mouse button is clicked while the cursor hot spot is in the window of another thread.



## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application calls this function after calling the <a href="/windows/desktop/api/winuser/nf-winuser-setcapture">SetCapture</a> function. 


#### Examples

For an example, see <a href="/windows/desktop/inputdev/using-mouse-input">Drawing Lines with the Mouse</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getcapture">GetCapture</a>



<a href="/windows/desktop/inputdev/mouse-input">Mouse Input</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcapture">SetCapture</a>



<a href="/windows/desktop/inputdev/wm-capturechanged">WM_CAPTURECHANGED</a>
