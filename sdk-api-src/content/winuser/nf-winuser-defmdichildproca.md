---
UID: NF:winuser.DefMDIChildProcA
title: DefMDIChildProcA function (winuser.h)
description: Provides default processing for any window message that the window procedure of a multiple-document interface (MDI) child window does not process. (ANSI)
helpviewer_keywords: ["DefMDIChildProcA", "winuser/DefMDIChildProcA"]
old-location: winmsg\defmdichildproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface\multipledocumentinterfacereference\multipledocumentinterfacefunctions\defmdichildproc.htm
ms.date: 12/05/2018
ms.keywords: DefMDIChildProc, DefMDIChildProc function [Windows and Messages], DefMDIChildProcA, DefMDIChildProcW, _win32_DefMDIChildProc, _win32_defmdichildproc_cpp, winmsg.defmdichildproc, winui._win32_defmdichildproc, winuser/DefMDIChildProc, winuser/DefMDIChildProcA, winuser/DefMDIChildProcW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DefMDIChildProcW (Unicode) and DefMDIChildProcA (ANSI)
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
 - DefMDIChildProcA
 - winuser/DefMDIChildProcA
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
 - DefMDIChildProc
 - DefMDIChildProcA
 - DefMDIChildProcW
---

# DefMDIChildProcA function


## -description

Provides default processing for any window message that the window procedure of a multiple-document interface (MDI) child window does not process. A window message not processed by the window procedure must be passed to the <b>DefMDIChildProc</b> function, not to the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the MDI child window.

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

The return value specifies the result of the message processing and depends on the message.

## -remarks

The <b>DefMDIChildProc</b> function assumes that the parent window of the MDI child window identified by the <i>hWnd</i> parameter was created with the <b>MDICLIENT</b> class. 

When an application's window procedure does not handle a message, it typically passes the message to the <a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function to process the message. MDI applications use the <a href="/windows/desktop/api/winuser/nf-winuser-defframeproca">DefFrameProc</a> and <b>DefMDIChildProc</b> functions instead of <b>DefWindowProc</b> to provide default message processing. All messages that an application would usually pass to <b>DefWindowProc</b> (such as nonclient messages and the <a href="/windows/desktop/winmsg/wm-settext">WM_SETTEXT</a> message) should be passed to <b>DefMDIChildProc</b> instead. In addition, <b>DefMDIChildProc</b> also handles the following messages. 

				

<table class="clsStd">
<tr>
<th>Message</th>
<th>Response</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/winmsg/wm-childactivate">WM_CHILDACTIVATE</a>
</td>
<td>Performs activation processing when MDI child windows are sized, moved, or displayed. This message must be passed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/winmsg/wm-getminmaxinfo">WM_GETMINMAXINFO</a>
</td>
<td>Calculates the size of a maximized MDI child window, based on the current size of the MDI client window.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/menurc/wm-menuchar">WM_MENUCHAR</a>
</td>
<td>Passes the message to the MDI frame window.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/winmsg/wm-move">WM_MOVE</a>
</td>
<td>Recalculates MDI client scroll bars if they are present.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/inputdev/wm-setfocus">WM_SETFOCUS</a>
</td>
<td>Activates the child window if it is not the active MDI child window.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/winmsg/wm-size">WM_SIZE</a>
</td>
<td>Performs operations necessary for changing the size of a window, especially for maximizing or restoring an MDI child window. Failing to pass this message to the <b>DefMDIChildProc</b> function produces highly undesirable results.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a>
</td>
<td>Handles window menu commands: <b>SC_NEXTWINDOW</b>, <b>SC_PREVWINDOW</b>, <b>SC_MOVE</b>, <b>SC_SIZE</b>, and <b>SC_MAXIMIZE</b>.</td>
</tr>
</table>
 





> [!NOTE]
> The winuser.h header defines DefMDIChildProc as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-defframeproca">DefFrameProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a>



<a href="/windows/desktop/winmsg/multiple-document-interface">Multiple Document Interface</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-childactivate">WM_CHILDACTIVATE</a>



<a href="/windows/desktop/winmsg/wm-getminmaxinfo">WM_GETMINMAXINFO</a>



<a href="/windows/desktop/menurc/wm-menuchar">WM_MENUCHAR</a>



<a href="/windows/desktop/winmsg/wm-move">WM_MOVE</a>



<a href="/windows/desktop/inputdev/wm-setfocus">WM_SETFOCUS</a>



<a href="/windows/desktop/winmsg/wm-settext">WM_SETTEXT</a>



<a href="/windows/desktop/winmsg/wm-size">WM_SIZE</a>



<a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a>
