---
UID: NF:winuser.TranslateAcceleratorW
title: TranslateAcceleratorW function
author: windows-sdk-content
description: Processes accelerator keys for menu commands.
old-location: menurc\translateaccelerator.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorfunctions\translateaccelerator.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: TranslateAccelerator, TranslateAccelerator function [Menus and Other Resources], TranslateAcceleratorA, TranslateAcceleratorW, _win32_TranslateAccelerator, _win32_translateaccelerator_cpp, menurc.translateaccelerator, winui._win32_translateaccelerator, winuser/TranslateAccelerator, winuser/TranslateAcceleratorA, winuser/TranslateAcceleratorW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TranslateAcceleratorW function


## -description


Processes accelerator keys for menu commands. The function translates a <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a> or <a href="https://msdn.microsoft.com/en-us/library/ms646286(v=VS.85).aspx">WM_SYSKEYDOWN</a> message to a <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> or <a href="https://msdn.microsoft.com/en-us/library/ms646360(v=VS.85).aspx">WM_SYSCOMMAND</a> message (if there is an entry for the key in the specified accelerator table) and then sends the <b>WM_COMMAND</b> or <b>WM_SYSCOMMAND</b> message directly to the specified window procedure. <b>TranslateAccelerator</b> does not return until the window procedure has processed the message.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose messages are to be translated.


### -param hAccTable [in]

Type: <b>HACCEL</b>

A handle to the accelerator table. The accelerator table must have been loaded by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms646370(v=VS.85).aspx">LoadAccelerators</a> function or created by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms646365(v=VS.85).aspx">CreateAcceleratorTable</a> function.


### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a> structure that contains message information retrieved from the calling thread's message queue using the <a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a> or <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a> function.


## -returns



Type: <b>int</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To differentiate the message that this function sends from messages sent by menus or controls, the high-order word of the
        <i>wParam</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> or <a href="https://msdn.microsoft.com/en-us/library/ms646360(v=VS.85).aspx">WM_SYSCOMMAND</a> message contains the value 1.

Accelerator key combinations used to select items from the
        <b>window</b> menu are translated into <a href="https://msdn.microsoft.com/en-us/library/ms646360(v=VS.85).aspx">WM_SYSCOMMAND</a> messages; all other accelerator key combinations are translated into <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> messages.

When <b>TranslateAccelerator</b> returns a nonzero value and the message is translated, the application should not use the <a href="https://msdn.microsoft.com/en-us/library/ms644955(v=VS.85).aspx">TranslateMessage</a> function to process the message again.

An accelerator need not correspond to a menu command.

If the accelerator command corresponds to a menu item, the application is sent <a href="https://msdn.microsoft.com/en-us/library/ms646344(v=VS.85).aspx">WM_INITMENU</a> and <a href="https://msdn.microsoft.com/en-us/library/ms646347(v=VS.85).aspx">WM_INITMENUPOPUP</a> messages, as if the user were trying to display the menu. However, these messages are not sent if any of the following conditions exist:

<ul>
<li>The window is disabled.</li>
<li>The accelerator key combination does not correspond to an item on the <b>window</b> menu and the window is minimized.</li>
<li>A mouse capture is in effect. For information about mouse capture, see the <a href="https://msdn.microsoft.com/en-us/library/ms646262(v=VS.85).aspx">SetCapture</a> function.</li>
</ul>
If the specified window is the active window and no window has the keyboard focus (which is generally the case if the window is minimized), <b>TranslateAccelerator</b> translates
        <a href="https://msdn.microsoft.com/en-us/library/ms646287(v=VS.85).aspx">WM_SYSKEYUP</a> and <a href="https://msdn.microsoft.com/en-us/library/ms646286(v=VS.85).aspx">WM_SYSKEYDOWN</a> messages instead of
        <a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a> and <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a> messages.

If an accelerator keystroke occurs that corresponds to a menu item when the window that owns the menu is minimized, <b>TranslateAccelerator</b> does not send a <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> message. However, if an accelerator keystroke occurs that does not match any of the items in the window's menu or in the
        <b>window</b> menu, the function sends a <b>WM_COMMAND</b> message, even if the window is minimized.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms646337(v=VS.85).aspx">Creating Accelerators for Font Attributes</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646365(v=VS.85).aspx">CreateAcceleratorTable</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645526(v=VS.85).aspx">Keyboard Accelerators</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646370(v=VS.85).aspx">LoadAccelerators</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646262(v=VS.85).aspx">SetCapture</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644955(v=VS.85).aspx">TranslateMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646344(v=VS.85).aspx">WM_INITMENU</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646347(v=VS.85).aspx">WM_INITMENUPOPUP</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646360(v=VS.85).aspx">WM_SYSCOMMAND</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646286(v=VS.85).aspx">WM_SYSKEYDOWN</a>
 

 

