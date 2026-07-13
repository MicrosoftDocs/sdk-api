---
UID: NF:winuser.DefFrameProcA
title: DefFrameProcA function (winuser.h)
description: Provides default processing for any window messages that the window procedure of a multiple-document interface (MDI) frame window does not process. (ANSI)
helpviewer_keywords: ["DefFrameProcA", "winuser/DefFrameProcA"]
old-location: winmsg\defframeproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface\multipledocumentinterfacereference\multipledocumentinterfacefunctions\defframeproc.htm
ms.date: 12/05/2018
ms.keywords: DefFrameProc, DefFrameProc function [Windows and Messages], DefFrameProcA, DefFrameProcW, _win32_DefFrameProc, _win32_defframeproc_cpp, winmsg.defframeproc, winui._win32_defframeproc, winuser/DefFrameProc, winuser/DefFrameProcA, winuser/DefFrameProcW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DefFrameProcW (Unicode) and DefFrameProcA (ANSI)
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
 - DefFrameProcA
 - winuser/DefFrameProcA
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
 - DefFrameProc
 - DefFrameProcA
 - DefFrameProcW
---

# DefFrameProcA function


## -description

Provides default processing for any window messages that the window procedure of a multiple-document interface (MDI) frame window does not process. All window messages that are not explicitly processed by the window procedure must be passed to the <b>DefFrameProc</b> function, not the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the MDI frame window.

### -param hWndMDIClient [in]

Type: <b>HWND</b>

A handle to the MDI client window.

### -param uMsg [in]

Type: <b>UINT</b>

The message to be processed.

### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.

### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>LRESULT</b>

The return value specifies the result of the message processing and depends on the message. If the <i>hWndMDIClient</i> parameter is <b>NULL</b>, the return value is the same as for the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function.

## -remarks

When an application's window procedure does not handle a message, it typically passes the message to the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function to process the message. MDI applications use the <b>DefFrameProc</b> and <a href="/windows/desktop/api/winuser/nf-winuser-defmdichildproca">DefMDIChildProc</a> functions instead of <b>DefWindowProc</b> to provide default message processing. All messages that an application would usually pass to <b>DefWindowProc</b> (such as nonclient messages and the <a href="/windows/desktop/winmsg/wm-settext">WM_SETTEXT</a> message) should be passed to <b>DefFrameProc</b> instead. The <b>DefFrameProc</b> function also handles the following messages. 

				

<table class="clsStd">
<tr>
<th>Message</th>
<th>Response</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a>
</td>
<td>Activates the MDI child window that the user chooses. This message is sent when the user chooses an MDI child window from the window menu of the MDI frame window. The window identifier accompanying this message identifies the MDI child window to be activated.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/menurc/wm-menuchar">WM_MENUCHAR</a>
</td>
<td>Opens the window menu of the active MDI child window when the user presses the ALT+ – (minus) key combination.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/inputdev/wm-setfocus">WM_SETFOCUS</a>
</td>
<td>Passes the keyboard focus to the MDI client window, which in turn passes it to the active MDI child window.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/winmsg/wm-size">WM_SIZE</a>
</td>
<td>Resizes the MDI client window to fit in the new frame window's client area. If the frame window procedure sizes the MDI client window to a different size, it should not pass the message to the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function.</td>
</tr>
</table>
 





> [!NOTE]
> The winuser.h header defines DefFrameProc as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-defmdichildproca">DefMDIChildProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a>



<a href="/windows/desktop/winmsg/multiple-document-interface">Multiple Document Interface</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-settext">WM_SETTEXT</a>
