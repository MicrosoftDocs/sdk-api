---
UID: NC:winuser.HOOKPROC
title: HOOKPROC (winuser.h)
description: An application-defined or library-defined callback function used with the SetWindowsHookEx function. The system calls this function after the SendMessage function is called. The hook procedure can examine the message; it cannot modify it.
helpviewer_keywords: ["CallWndRetProc","CallWndRetProc callback","CallWndRetProc callback function [Windows and Messages]","HOOKPROC","_win32_CallWndRetProc","_win32_callwndretproc_cpp","winmsg.callwndretproc","winui._win32_callwndretproc","winuser/CallWndRetProc"]
old-location: winmsg\callwndretproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\callwndretproc.htm
ms.date: 12/05/2018
ms.keywords: CallWndRetProc, CallWndRetProc callback, CallWndRetProc callback function [Windows and Messages], HOOKPROC, _win32_CallWndRetProc, _win32_callwndretproc_cpp, winmsg.callwndretproc, winui._win32_callwndretproc, winuser/CallWndRetProc
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HOOKPROC
 - winuser/HOOKPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - CallWndRetProc
---

# HOOKPROC callback function


## -description

An application-defined or library-defined callback function used with the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a> function. The system calls this function after the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function is called. The hook procedure can examine the message; it cannot modify it.

The <b>HOOKPROC</b> type defines a pointer to this callback function. <i>CallWndRetProc</i> is a placeholder for the application-defined or library-defined function name.

## -parameters

### -param code

### -param wParam [in]

Type: <b>WPARAM</b>

Specifies whether the message is sent by the current process. If the message is sent by the current process, it is nonzero; otherwise, it is <b>NULL</b>.

### -param lParam [in]

Type: <b>LPARAM</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-cwpretstruct">CWPRETSTRUCT</a> structure that contains details about the message. 


#### - nCode [in]

Type: <b>int</b>

Specifies whether the hook procedure must process the message. If <i>nCode</i> is <b>HC_ACTION</b>, the hook procedure must process the message. If 	<i>nCode</i> is less than zero, the hook procedure must pass the message to the [CallNextHookEx function](nf-winuser-callnexthookex.md) function without further processing and should return the value returned by <b>CallNextHookEx</b>.

## -returns

Type: <b>LRESULT</b>

If <i>nCode</i> is less than zero, the hook procedure must return the value returned by [CallNextHookEx function](nf-winuser-callnexthookex.md). 

If <i>nCode</i> is greater than or equal to zero, it is highly recommended that you call [CallNextHookEx function](nf-winuser-callnexthookex.md) and return the value it returns; otherwise, other applications that have installed <a href="/windows/desktop/winmsg/about-hooks">WH_CALLWNDPROCRET</a> hooks will not receive hook notifications and may behave incorrectly as a result. If the hook procedure does not call <b>CallNextHookEx</b>, the return value should be zero.

## -remarks

An application installs the hook procedure by specifying the <a href="/windows/desktop/winmsg/about-hooks">WH_CALLWNDPROCRET</a> hook type and a pointer to the hook procedure in a call to the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a> function.

## -see-also

[CWPRETSTRUCT structure](ns-winuser-cwpretstruct.md), [CallNextHookEx function](nf-winuser-callnexthookex.md), [CallWindowProcW function](nf-winuser-callwindowprocw.md), [CallWindowProcA function](nf-winuser-callwindowproca.md), [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa), [Hooks](/windows/desktop/winmsg/hooks)
