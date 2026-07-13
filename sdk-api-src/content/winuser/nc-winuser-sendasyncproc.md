---
UID: NC:winuser.SENDASYNCPROC
title: SENDASYNCPROC (winuser.h)
description: An application-defined callback function used with the SendMessageCallback function.
helpviewer_keywords: ["SendAsyncProc","SendAsyncProc callback","SendAsyncProc callback function [Windows and Messages]","_win32_SendAsyncProc","_win32_sendasyncproc_cpp","winmsg.sendasyncproc","winui._win32_sendasyncproc","winuser/SendAsyncProc"]
old-location: winmsg\sendasyncproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendasyncproc.htm
ms.date: 09/30/2025
ms.keywords: SendAsyncProc, SendAsyncProc callback, SendAsyncProc callback function [Windows and Messages], _win32_SendAsyncProc, _win32_sendasyncproc_cpp, winmsg.sendasyncproc, winui._win32_sendasyncproc, winuser/SendAsyncProc
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
 - SENDASYNCPROC
 - winuser/SENDASYNCPROC
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
 - SendAsyncProc
---

# SENDASYNCPROC callback function

## -description

An application-defined callback function used with the [SendMessageCallback](/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka) function. The system passes the message to the callback function after passing the message to the destination window procedure. The **SENDASYNCPROC** type defines a pointer to this callback function. _SendAsyncProc_ is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

Type: **HWND**

A handle to the window whose window procedure received the message. This parameter is typically named _hWnd_.

If the [SendMessageCallback](/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka) function was called with its _hWnd_ parameter set to **HWND_BROADCAST**, the system calls the _SendAsyncProc_ function once for each top-level window.

### -param unnamedParam2

Type: **UINT**

The message. This parameter is typically named _uMsg_.

### -param unnamedParam3

Type: **ULONG_PTR**

An application-defined value sent from the [SendMessageCallback](/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka) function. This parameter is typically named _dwData_.

### -param unnamedParam4

Type: **LRESULT**

The result of the message processing. This value depends on the message. This parameter is typically named _lResult_.

## -remarks

> [!NOTE]
> The parameters are defined in the header with no names: `typedef VOID (CALLBACK* SENDASYNCPROC)(HWND, UINT, ULONG_PTR, LRESULT);`. Therefore, the syntax block lists them as `unnamedParam1` - `unnamedParam4`. You can name these parameters anything in your app. However, they are usually named as shown in the parameter descriptions.

You install a _SendAsyncProc_ application-defined callback function by passing a **SENDASYNCPROC** pointer to the [SendMessageCallback](/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka) function.

The callback function is only called when the thread that called [SendMessageCallback](/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka) calls [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage), [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagea), or [WaitMessage](/windows/desktop/api/winuser/nf-winuser-waitmessage).

## -see-also

**Conceptual**

[Messages and Message Queues](/windows/desktop/winmsg/messages-and-message-queues)

**Reference**

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagea)

[SendMessageCallback](/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka)

[WaitMessage](/windows/desktop/api/winuser/nf-winuser-waitmessage)