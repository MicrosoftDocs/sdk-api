---
UID: NF:winuser.GetWindowTextA
title: GetWindowTextA function (winuser.h)
description: Copies the text of the specified window's title bar (if it has one) into a buffer. If the specified window is a control, the text of the control is copied. However, GetWindowText cannot retrieve the text of a control in another application. (ANSI)
helpviewer_keywords: ["GetWindowTextA", "winuser/GetWindowTextA"]
old-location: winmsg\getwindowtext.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowtext.htm
ms.date: 12/05/2018
ms.keywords: GetWindowText, GetWindowText function [Windows and Messages], GetWindowTextA, GetWindowTextW, _win32_GetWindowText, _win32_getwindowtext_cpp, winmsg.getwindowtext, winui._win32_getwindowtext, winuser/GetWindowText, winuser/GetWindowTextA, winuser/GetWindowTextW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetWindowTextW (Unicode) and GetWindowTextA (ANSI)
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
ms.custom: snippet-project
f1_keywords:
 - GetWindowTextA
 - winuser/GetWindowTextA
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
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetWindowText
 - GetWindowTextA
 - GetWindowTextW
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# GetWindowTextA function


## -description

Copies the text of the specified window's title bar (if it has one) into a buffer. If the specified window is a control, the text of the control is copied. However, <b>GetWindowText</b> cannot retrieve the text of a control in another application.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window or control containing the text.

### -param lpString [out]

Type: <b>LPTSTR</b>

The buffer that will receive the text. If the string is as long or longer than the buffer, the string is truncated and terminated with a null character.

### -param nMaxCount [in]

Type: <b>int</b>

The maximum number of characters to copy to the buffer, including the null character. If the text exceeds this limit, it is truncated.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the length, in characters, of the copied string, not including the terminating null character. If the window has no title bar or text, if the title bar is empty, or if the window or control handle is invalid, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

This function cannot retrieve the text of an edit control in another application.

## -remarks

If the target window is owned by the current process, <b>GetWindowText</b> causes a <a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a> message to be sent to the specified window or control. If the target window is owned by another process and has a caption, <b>GetWindowText</b> retrieves the window caption text. If the window does not have a caption, the return value is a null string. This behavior is by design. It allows applications to call <b>GetWindowText</b> without becoming unresponsive if the process that owns the target window is not responding. However, if the target window is not responding and it belongs to the calling application, <b>GetWindowText</b> will cause the calling application to become unresponsive. 

To retrieve the text of a control in another process, send a <a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a> message directly instead of calling <b>GetWindowText</b>. 


#### Examples

The following example code demonstrates a call to **GetWindowTextA**.

```cpp
hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
cTxtLen = GetWindowTextLength(hwndCombo); 

// Allocate memory for the string and copy 
// the string into the memory. 

pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
    PAGE_READWRITE); 
GetWindowText(hwndCombo, pszMem, 
    cTxtLen + 1); 
```

 To see this example in context, see <a href="/windows/desktop/winmsg/using-messages-and-message-queues">Sending a Message</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines GetWindowText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha">GetWindowTextLength</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowtexta">SetWindowText</a>



<a href="/windows/desktop/winmsg/wm-gettext">WM_GETTEXT</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
