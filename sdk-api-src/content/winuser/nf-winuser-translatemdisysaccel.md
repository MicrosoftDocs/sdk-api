---
UID: NF:winuser.TranslateMDISysAccel
title: TranslateMDISysAccel function (winuser.h)
description: Processes accelerator keystrokes for window menu commands of the multiple-document interface (MDI) child windows associated with the specified MDI client window.
helpviewer_keywords: ["TranslateMDISysAccel","TranslateMDISysAccel function [Windows and Messages]","_win32_TranslateMDISysAccel","_win32_translatemdisysaccel_cpp","winmsg.translatemdisysaccel","winui._win32_translatemdisysaccel","winuser/TranslateMDISysAccel"]
old-location: winmsg\translatemdisysaccel.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface\multipledocumentinterfacereference\multipledocumentinterfacefunctions\translatemdisysaccel.htm
ms.date: 12/05/2018
ms.keywords: TranslateMDISysAccel, TranslateMDISysAccel function [Windows and Messages], _win32_TranslateMDISysAccel, _win32_translatemdisysaccel_cpp, winmsg.translatemdisysaccel, winui._win32_translatemdisysaccel, winuser/TranslateMDISysAccel
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
 - TranslateMDISysAccel
 - winuser/TranslateMDISysAccel
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
 - TranslateMDISysAccel
---

# TranslateMDISysAccel function


## -description

Processes accelerator keystrokes for window menu commands of the multiple-document interface (MDI) child windows associated with the specified MDI client window. The function translates <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a> and <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a> messages to <a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a> messages and sends them to the appropriate MDI child windows.

## -parameters

### -param hWndClient [in]

Type: <b>HWND</b>

A handle to the MDI client window.

### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to a message retrieved by using the <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> function. The message must be an <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure and contain message information from the application's message queue.

## -returns

Type: <b>BOOL</b>

If the message is translated into a system command, the return value is nonzero.

If the message is not translated into a system command, the return value is zero.

## -see-also

- <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>
- <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>
- <a href="/windows/desktop/winmsg/multiple-document-interface">Multiple Document Interface</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-translateacceleratora">TranslateAccelerator</a>
- <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>
- <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>
- <a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>