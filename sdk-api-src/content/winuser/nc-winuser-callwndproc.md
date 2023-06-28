---
UID: NC:winuser.CALLWNDPROC
title: CALLWNDPROC (winuser.h)
description: Application-defined or library-defined callback function used with the SetWindowsHookEx function.
helpviewer_keywords: ["CALLWNDPROC","CALLWNDPROC callback","CALLWNDPROC callback function","_win32_CallWndProc","_win32_callwndproc_cpp","winui._win32_callwndproc","winuser/CALLWNDPROC"]
tech.root: winmsg
ms.date: 12/05/2018
ms.keywords: CALLWNDPROC, CALLWNDPROC callback, CALLWNDPROC callback function, _win32_CallWndProc, _win32_callwndproc_cpp, winui._win32_callwndproc, winuser/CALLWNDPROC
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
f1_keywords:
- CallWndProc
- winuser/CallWndProc
dev_langs:
- C++
- C
api_location:
- Winuser.h
api_type:
- UserDefined
product:
- Windows
topic_type:
- apiref
- kbSyntax
api_name:
- CallWndProc
---

# CallWndProc callback function

An application-defined or library-defined callback function used with the [**SetWindowsHookEx**](https://msdn.microsoft.com/en-us/library/ms644990\(v=vs.85\)) function. The system calls this function before calling the window procedure to process a message sent to the thread.

The **HOOKPROC** type defines a pointer to this callback function. *CallWndProc* is a placeholder for the application-defined or library-defined function name.

## Syntax

```cpp
LRESULT CALLBACK CallWndProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## -parameters

### -param nCode [in]

Type: **int**

Specifies whether the hook procedure must process the message. If *nCode* is **HC\_ACTION**, the hook procedure must process the message. If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx function](nf-winuser-callnexthookex.md) function without further processing and must return the value returned by **CallNextHookEx**.

### -param wParam [in]

Type: **WPARAM**

Specifies whether the message was sent by the current thread. If the message was sent by the current thread, it is nonzero; otherwise, it is zero.
    
### -param lParam [in]

Type: **LPARAM**

A pointer to a [CWPSTRUCT structure](ns-winuser-cwpstruct.md) that contains details about the message.    

## Return value

Type: LRESULT

If *nCode* is less than zero, the hook procedure must return the value returned by [**CallNextHookEx function**](nf-winuser-callnexthookex.md).

If *nCode* is greater than or equal to zero, it is highly recommended that you call **CallNextHookEx** function and return the value it returns; otherwise, other applications that have installed [**WH\_CALLWNDPROC**](https://msdn.microsoft.com/en-us/library/ms644959\(v=vs.85\)) hooks will not receive hook notifications and may behave incorrectly as a result. If the hook procedure does not call **CallNextHookEx**, the return value should be zero.

## Remarks

The *CallWndProc* hook procedure can examine the message, but it cannot modify it. After the hook procedure returns control to the system, the message is passed to the window procedure.

An application installs the hook procedure by specifying the [**WH_CALLWNDPROC**](/windows/win32/winmsg/about-hooks#wh_callwndproc-and-wh_callwndprocret) hook type and a pointer to the hook procedure in a call to the [SetWindowsHookExA function](nf-winuser-setwindowshookexa.md)/[SetWindowsHookExW function](nf-winuser-setwindowshookexw.md) function.

## See also

[CallNextHookEx function](nf-winuser-callnexthookex.md), [SetWindowsHookExA function](nf-winuser-setwindowshookexa.md), [SetWindowsHookExW function](nf-winuser-setwindowshookexw.md), [CWPSTRUCT structure](ns-winuser-cwpstruct.md), [SendMessage function](nf-winuser-sendmessage.md), [Hooks](/windows/win32/winmsg/hooks)
