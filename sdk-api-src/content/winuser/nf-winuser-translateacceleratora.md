---
UID: NF:winuser.TranslateAcceleratorA
title: TranslateAcceleratorA function
author: windows-sdk-content
description: Processes accelerator keys for menu commands.
old-location: menurc\translateaccelerator.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorfunctions\translateaccelerator.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: TranslateAccelerator, TranslateAccelerator function [Menus and Other Resources], TranslateAcceleratorA, TranslateAcceleratorW, _win32_TranslateAccelerator, _win32_translateaccelerator_cpp, menurc.translateaccelerator, winui._win32_translateaccelerator, winuser/TranslateAccelerator, winuser/TranslateAcceleratorA, winuser/TranslateAcceleratorW
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AR_STATE, *PAR_STATE
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# TranslateAcceleratorA function


## -description


Processes accelerator keys for menu commands. The function translates a <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a> or <a href="https://msdn.microsoft.com/a3c03dbf-1be7-49ff-b931-1981786b74ce">WM_SYSKEYDOWN</a> message to a <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> or <a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a> message (if there is an entry for the key in the specified accelerator table) and then sends the <b>WM_COMMAND</b> or <b>WM_SYSCOMMAND</b> message directly to the specified window procedure. <b>TranslateAccelerator</b> does not return until the window procedure has processed the message.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose messages are to be translated.


### -param hAccTable [in]

Type: <b>HACCEL</b>

A handle to the accelerator table. The accelerator table must have been loaded by a call to the <a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a> function or created by a call to the <a href="https://msdn.microsoft.com/ea8ba5dd-0fa8-4cab-9f48-69fb5cd38a51">CreateAcceleratorTable</a> function.


### -param lpMsg [in]

Type: <b>LPMSG</b>

A pointer to an <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure that contains message information retrieved from the calling thread's message queue using the <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> or <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a> function.


## -returns



Type: <b>int</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To differentiate the message that this function sends from messages sent by menus or controls, the high-order word of the
        <i>wParam</i> parameter of the <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> or <a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a> message contains the value 1.

Accelerator key combinations used to select items from the
        <b>window</b> menu are translated into <a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a> messages; all other accelerator key combinations are translated into <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> messages.

When <b>TranslateAccelerator</b> returns a nonzero value and the message is translated, the application should not use the <a href="https://msdn.microsoft.com/41c2baf4-6426-4789-919c-ab8ff9be8679">TranslateMessage</a> function to process the message again.

An accelerator need not correspond to a menu command.

If the accelerator command corresponds to a menu item, the application is sent <a href="https://msdn.microsoft.com/d0fcc6d8-f57c-4d04-b9e7-4cfab6add173">WM_INITMENU</a> and <a href="https://msdn.microsoft.com/08ae1a78-5e68-488c-9b77-ee42044ca3ab">WM_INITMENUPOPUP</a> messages, as if the user were trying to display the menu. However, these messages are not sent if any of the following conditions exist:

<ul>
<li>The window is disabled.</li>
<li>The accelerator key combination does not correspond to an item on the <b>window</b> menu and the window is minimized.</li>
<li>A mouse capture is in effect. For information about mouse capture, see the <a href="https://msdn.microsoft.com/f97cf81d-1f4c-4677-8e39-ca23f07aa95d">SetCapture</a> function.</li>
</ul>
If the specified window is the active window and no window has the keyboard focus (which is generally the case if the window is minimized), <b>TranslateAccelerator</b> translates
        <a href="https://msdn.microsoft.com/a4f62575-fb84-4390-a1d1-1a62629de55f">WM_SYSKEYUP</a> and <a href="https://msdn.microsoft.com/a3c03dbf-1be7-49ff-b931-1981786b74ce">WM_SYSKEYDOWN</a> messages instead of
        <a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a> and <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a> messages.

If an accelerator keystroke occurs that corresponds to a menu item when the window that owns the menu is minimized, <b>TranslateAccelerator</b> does not send a <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> message. However, if an accelerator keystroke occurs that does not match any of the items in the window's menu or in the
        <b>window</b> menu, the function sends a <b>WM_COMMAND</b> message, even if the window is minimized.


#### Examples

For an example, see <a href="https://www.bing.com/search?q=Creating+Accelerators+for+Font+Attributes">Creating Accelerators for Font Attributes</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ea8ba5dd-0fa8-4cab-9f48-69fb5cd38a51">CreateAcceleratorTable</a>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/cb5e268d-8e38-4682-a736-ecf9bcc34acd">Keyboard Accelerators</a>



<a href="https://msdn.microsoft.com/52ead129-a4fe-413a-a86a-349d4bd816db">LoadAccelerators</a>



<a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>



<a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f97cf81d-1f4c-4677-8e39-ca23f07aa95d">SetCapture</a>



<a href="https://msdn.microsoft.com/41c2baf4-6426-4789-919c-ab8ff9be8679">TranslateMessage</a>



<a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a>



<a href="https://msdn.microsoft.com/d0fcc6d8-f57c-4d04-b9e7-4cfab6add173">WM_INITMENU</a>



<a href="https://msdn.microsoft.com/08ae1a78-5e68-488c-9b77-ee42044ca3ab">WM_INITMENUPOPUP</a>



<a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>



<a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a>



<a href="https://msdn.microsoft.com/a3c03dbf-1be7-49ff-b931-1981786b74ce">WM_SYSKEYDOWN</a>
 

 

