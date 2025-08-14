---
UID: NF:winuser.TranslateAcceleratorW
title: TranslateAcceleratorW function (winuser.h)
description: Processes accelerator keys for menu commands. (Unicode)
helpviewer_keywords: ["TranslateAccelerator", "TranslateAccelerator function [Menus and Other Resources]", "TranslateAcceleratorW", "_win32_TranslateAccelerator", "_win32_translateaccelerator_cpp", "menurc.translateaccelerator", "winui._win32_translateaccelerator", "winuser/TranslateAccelerator", "winuser/TranslateAcceleratorW"]
old-location: menurc\translateaccelerator.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorfunctions\translateaccelerator.htm
ms.date: 12/05/2018
ms.keywords: TranslateAccelerator, TranslateAccelerator function [Menus and Other Resources], TranslateAcceleratorA, TranslateAcceleratorW, _win32_TranslateAccelerator, _win32_translateaccelerator_cpp, menurc.translateaccelerator, winui._win32_translateaccelerator, winuser/TranslateAccelerator, winuser/TranslateAcceleratorA, winuser/TranslateAcceleratorW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TranslateAcceleratorW (Unicode) and TranslateAcceleratorA (ANSI)
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
 - TranslateAcceleratorW
 - winuser/TranslateAcceleratorW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-keyboard-l1-3-2.dll
 - ext-ms-win-ntuser-keyboard-l1-3-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - api-ms-win-ntuser-ie-keyboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - TranslateAccelerator
 - TranslateAcceleratorA
 - TranslateAcceleratorW
---

# TranslateAcceleratorW function


## -description

Processes accelerator keys for menu commands. The function translates a <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a> or <a href="/windows/desktop/inputdev/wm-syskeydown">WM_SYSKEYDOWN</a> message to a <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> or <a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a> message (if there is an entry for the key in the specified accelerator table) and then sends the <b>WM_COMMAND</b> or <b>WM_SYSCOMMAND</b> message directly to the specified window procedure. <b>TranslateAccelerator</b> does not return until the window procedure has processed the message.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose messages are to be translated.

### -param hAccTable [in]

Type: <b>HACCEL</b>

A handle to the accelerator table. The accelerator table must have been loaded by a call to the <a href="/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa">LoadAccelerators</a> function or created by a call to the <a href="/windows/desktop/api/winuser/nf-winuser-createacceleratortablea">CreateAcceleratorTable</a> function.

### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that contains message information retrieved from the calling thread's message queue using the <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> function.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To differentiate the message that this function sends from messages sent by menus or controls, the high-order word of the
        <i>wParam</i> parameter of the <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> or <a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a> message contains the value 1.

Accelerator key combinations used to select items from the
        <b>window</b> menu are translated into <a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a> messages; all other accelerator key combinations are translated into <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> messages.

When <b>TranslateAccelerator</b> returns a nonzero value and the message is translated, the application should not use the <a href="/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a> function to process the message again.

An accelerator need not correspond to a menu command.

If the accelerator command corresponds to a menu item, the application is sent <a href="/windows/desktop/menurc/wm-initmenu">WM_INITMENU</a> and <a href="/windows/desktop/menurc/wm-initmenupopup">WM_INITMENUPOPUP</a> messages, as if the user were trying to display the menu. However, these messages are not sent if any of the following conditions exist:

<ul>
<li>The window is disabled.</li>
<li>The accelerator key combination does not correspond to an item on the <b>window</b> menu and the window is minimized.</li>
<li>A mouse capture is in effect. For information about mouse capture, see the <a href="/windows/desktop/api/winuser/nf-winuser-setcapture">SetCapture</a> function.</li>
</ul>
If the specified window is the active window and no window has the keyboard focus (which is generally the case if the window is minimized), <b>TranslateAccelerator</b> translates
        <a href="/windows/desktop/inputdev/wm-syskeyup">WM_SYSKEYUP</a> and <a href="/windows/desktop/inputdev/wm-syskeydown">WM_SYSKEYDOWN</a> messages instead of
        <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a> and <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a> messages.

If an accelerator keystroke occurs that corresponds to a menu item when the window that owns the menu is minimized, <b>TranslateAccelerator</b> does not send a <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message. However, if an accelerator keystroke occurs that does not match any of the items in the window's menu or in the
        <b>window</b> menu, the function sends a <b>WM_COMMAND</b> message, even if the window is minimized.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-keyboard-accelerators">Creating Accelerators for Font Attributes</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines TranslateAccelerator as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

- <a href="/windows/desktop/api/winuser/nf-winuser-createacceleratortablea">CreateAcceleratorTable</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>
- <a href="/windows/desktop/menurc/keyboard-accelerators">Keyboard Accelerators</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa">LoadAccelerators</a>
- <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-setcapture">SetCapture</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a>
- <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a>
- <a href="/windows/desktop/menurc/wm-initmenu">WM_INITMENU</a>
- <a href="/windows/desktop/menurc/wm-initmenupopup">WM_INITMENUPOPUP</a>
- <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>
- <a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a>
- <a href="/windows/desktop/inputdev/wm-syskeydown">WM_SYSKEYDOWN</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>
