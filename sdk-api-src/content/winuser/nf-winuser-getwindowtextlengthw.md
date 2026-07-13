---
UID: NF:winuser.GetWindowTextLengthW
title: GetWindowTextLengthW function (winuser.h)
description: Retrieves the length, in characters, of the specified window's title bar text (if the window has a title bar). (Unicode)
helpviewer_keywords: ["GetWindowTextLength", "GetWindowTextLength function [Windows and Messages]", "GetWindowTextLengthW", "_win32_GetWindowTextLength", "_win32_getwindowtextlength_cpp", "winmsg.getwindowtextlength", "winui._win32_getwindowtextlength", "winuser/GetWindowTextLength", "winuser/GetWindowTextLengthW"]
old-location: winmsg\getwindowtextlength.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowtextlength.htm
ms.date: 12/05/2018
ms.keywords: GetWindowTextLength, GetWindowTextLength function [Windows and Messages], GetWindowTextLengthA, GetWindowTextLengthW, _win32_GetWindowTextLength, _win32_getwindowtextlength_cpp, winmsg.getwindowtextlength, winui._win32_getwindowtextlength, winuser/GetWindowTextLength, winuser/GetWindowTextLengthA, winuser/GetWindowTextLengthW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetWindowTextLengthW (Unicode) and GetWindowTextLengthA (ANSI)
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
 - GetWindowTextLengthW
 - winuser/GetWindowTextLengthW
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
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-0.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetWindowTextLength
 - GetWindowTextLengthA
 - GetWindowTextLengthW
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# GetWindowTextLengthW function


## -description

Retrieves the length, in characters, of the specified window's title bar text (if the window has a title bar). If the specified window is a control, the function retrieves the length of the text within the control. However, <b>GetWindowTextLength</b> cannot retrieve the length of the text of an edit control in another application.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window or control.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the length, in characters, of the text. Under certain conditions, this value might be greater than the length of the text (see Remarks).

If the window has no text, the return value is zero. 

Function failure is indicated by a return value of zero and a <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> result that is nonzero.

> [!NOTE]
> This function does not clear the most recent error information. To determine success or failure, clear the most recent error information by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> with 0, then call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the target window is owned by the current process, <b>GetWindowTextLength</b> causes a <a href="/windows/desktop/winmsg/wm-gettextlength">WM_GETTEXTLENGTH</a> message to be sent to the specified window or control. 

Under certain conditions, the <b>GetWindowTextLength</b> function may return a value that is larger than the actual length of the text. This occurs with certain mixtures of ANSI and Unicode, and is due to the system allowing for the possible existence of double-byte character set (DBCS) characters within the text. The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation. This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode. It can also occur when an application uses the ANSI version of <b>GetWindowTextLength</b> with a window whose window procedure is Unicode, or the Unicode version of <b>GetWindowTextLength</b> with a window whose window procedure is ANSI. For more information on ANSI and ANSI functions, see <a href="/windows/desktop/Intl/conventions-for-function-prototypes">Conventions for Function Prototypes</a>. 

To obtain the exact length of the text, use the <a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a>, <a href="/windows/desktop/Controls/lb-gettext">LB_GETTEXT</a>, or <a href="/windows/desktop/Controls/cb-getlbtext">CB_GETLBTEXT</a> messages, or the <a href="/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a> function.





> [!NOTE]
> The winuser.h header defines GetWindowTextLength as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Controls/cb-getlbtext">CB_GETLBTEXT</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a>



<a href="/windows/desktop/Controls/lb-gettext">LB_GETTEXT</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowtexta">SetWindowText</a>



<a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a>



<a href="/windows/desktop/winmsg/wm-gettextlength">WM_GETTEXTLENGTH</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
