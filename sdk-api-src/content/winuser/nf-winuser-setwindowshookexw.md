---
UID: NF:winuser.SetWindowsHookExW
title: SetWindowsHookExW function
author: windows-sdk-content
description: Installs an application-defined hook procedure into a hook chain.
old-location: winmsg\setwindowshookex.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\setwindowshookex.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: SetWindowsHookEx, SetWindowsHookEx function [Windows and Messages], SetWindowsHookExA, SetWindowsHookExW, WH_CALLWNDPROC, WH_CALLWNDPROCRET, WH_CBT, WH_DEBUG, WH_FOREGROUNDIDLE, WH_GETMESSAGE, WH_JOURNALPLAYBACK, WH_JOURNALRECORD, WH_KEYBOARD, WH_KEYBOARD_LL, WH_MOUSE, WH_MOUSE_LL, WH_MSGFILTER, WH_SHELL, WH_SYSMSGFILTER, _win32_SetWindowsHookEx, _win32_setwindowshookex_cpp, winmsg.setwindowshookex, winui._win32_setwindowshookex, winuser/SetWindowsHookEx, winuser/SetWindowsHookExA, winuser/SetWindowsHookExW
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
req.unicode-ansi: SetWindowsHookExW (Unicode) and SetWindowsHookExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetWindowsHookEx
 - SetWindowsHookExA
 - SetWindowsHookExW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetWindowsHookExW function


## -description


Installs an application-defined hook procedure into a hook chain. You would install a hook procedure to monitor the system for certain types of events. These events are associated either with a specific thread or with all threads in the same desktop as the calling thread. 


## -parameters




### -param idHook [in]

Type: <b>int</b>

The type of hook procedure to be installed. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WH_CALLWNDPROC"></a><a id="wh_callwndproc"></a><dl>
<dt><b>WH_CALLWNDPROC</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that monitors messages before the system sends them to the destination window procedure. For more information, see the <a href="https://msdn.microsoft.com/25df5ac2-f007-4683-ba89-537dc7a3c15e">CallWndProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_CALLWNDPROCRET"></a><a id="wh_callwndprocret"></a><dl>
<dt><b>WH_CALLWNDPROCRET</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that monitors messages after they have been processed by the destination window procedure. For more information, see the <a href="https://msdn.microsoft.com/4e666fae-add5-4ea5-a314-e034f894d493">CallWndRetProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_CBT"></a><a id="wh_cbt"></a><dl>
<dt><b>WH_CBT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that receives notifications useful to a CBT application. For more information, see the <a href="https://msdn.microsoft.com/26c48395-f0b8-4c03-bf65-d76cdf0117d6">CBTProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_DEBUG"></a><a id="wh_debug"></a><dl>
<dt><b>WH_DEBUG</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure useful for debugging other hook procedures. For more information, see the <a href="https://msdn.microsoft.com/d9d446a1-1337-4efa-bb33-9e5b762476f8">DebugProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_FOREGROUNDIDLE"></a><a id="wh_foregroundidle"></a><dl>
<dt><b>WH_FOREGROUNDIDLE</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that will be called when the application's foreground thread is about to become idle. This hook is useful for performing low priority tasks during idle time. For more information, see the <a href="https://msdn.microsoft.com/de6f5c7b-df4f-4b63-ac46-236c332de2a3">ForegroundIdleProc</a> hook procedure. 

</td>
</tr>
<tr>
<td width="40%"><a id="WH_GETMESSAGE"></a><a id="wh_getmessage"></a><dl>
<dt><b>WH_GETMESSAGE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that monitors messages posted to a message queue. For more information, see the <a href="https://msdn.microsoft.com/3d6a61eb-6c1d-4222-a627-c129822312b9">GetMsgProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_JOURNALPLAYBACK"></a><a id="wh_journalplayback"></a><dl>
<dt><b>WH_JOURNALPLAYBACK</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that posts messages previously recorded by a <a href="about_hooks.htm">WH_JOURNALRECORD</a> hook procedure. For more information, see the <a href="https://msdn.microsoft.com/ee7cfc0e-c04e-4f1c-bf03-e6ad770d4659">JournalPlaybackProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_JOURNALRECORD"></a><a id="wh_journalrecord"></a><dl>
<dt><b>WH_JOURNALRECORD</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that records input messages posted to the system message queue. This hook is useful for recording macros. For more information, see the <a href="https://msdn.microsoft.com/377cdb26-563b-4014-ac52-ef0c441e94b5">JournalRecordProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_KEYBOARD"></a><a id="wh_keyboard"></a><dl>
<dt><b>WH_KEYBOARD</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that monitors keystroke messages. For more information, see the <a href="https://msdn.microsoft.com/3fdcc0b4-013a-48e3-9a01-bf34953daddc">KeyboardProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_KEYBOARD_LL"></a><a id="wh_keyboard_ll"></a><dl>
<dt><b>WH_KEYBOARD_LL</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
 Installs a hook procedure that monitors low-level keyboard input events. For more information, see the <a href="https://msdn.microsoft.com/9d66accd-04cd-4839-b826-1c85dfb3b24e">LowLevelKeyboardProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_MOUSE"></a><a id="wh_mouse"></a><dl>
<dt><b>WH_MOUSE</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that monitors mouse messages. For more information, see the <a href="https://msdn.microsoft.com/4fc1d81d-ee12-4ee4-b29c-2450b92b83b5">MouseProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_MOUSE_LL"></a><a id="wh_mouse_ll"></a><dl>
<dt><b>WH_MOUSE_LL</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
 Installs a hook procedure that monitors low-level mouse input events. For more information, see the <a href="https://msdn.microsoft.com/a0922155-22e5-410a-b64e-f87690de8a17">LowLevelMouseProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_MSGFILTER"></a><a id="wh_msgfilter"></a><dl>
<dt><b>WH_MSGFILTER</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that monitors messages generated as a result of an input event in a dialog box, message box, menu, or scroll bar. For more information, see the <a href="https://msdn.microsoft.com/20f8511d-8160-4565-99b3-d373501b1bd1">MessageProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_SHELL"></a><a id="wh_shell"></a><dl>
<dt><b>WH_SHELL</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that receives notifications useful to shell applications. For more information, see the <a href="https://msdn.microsoft.com/4c21e0d8-2529-4b04-ad45-762ca7f1e5ef">ShellProc</a> hook procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="WH_SYSMSGFILTER"></a><a id="wh_sysmsgfilter"></a><dl>
<dt><b>WH_SYSMSGFILTER</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Installs a hook procedure that monitors messages generated as a result of an input event in a dialog box, message box, menu, or scroll bar. The hook procedure monitors these messages for all applications in the same desktop as the calling thread. For more information, see the <a href="https://msdn.microsoft.com/5ed3a4f0-8b7e-4896-b8d4-b5f071de895d">SysMsgProc</a> hook procedure.

</td>
</tr>
</table>
 


### -param lpfn [in]

Type: <b>HOOKPROC</b>

A pointer to the hook procedure. If the <i>dwThreadId</i> parameter is zero or specifies the identifier of a thread created by a different process, the <i>lpfn</i> parameter must point to a hook procedure in a DLL. Otherwise, <i>lpfn</i> can point to a hook procedure in the code associated with the current process. 


### -param hmod

TBD


### -param dwThreadId [in]

Type: <b>DWORD</b>

The identifier of the thread with which the hook procedure is to be associated. For desktop apps, if this parameter is zero, the hook procedure is associated with all existing threads running in the same desktop as the calling thread. For Windows Store apps, see the Remarks section.


#### - hMod [in]

Type: <b>HINSTANCE</b>

A handle to the DLL containing the hook procedure pointed to by the <i>lpfn</i> parameter. The <i>hMod</i> parameter must be set to <b>NULL</b> if the <i>dwThreadId</i> parameter specifies a thread created by the current process and if the hook procedure is within the code associated with the current process. 


## -returns



Type: <strong>Type: <b>HHOOK</b>
</strong>

If the function succeeds, the return value is the handle to the hook procedure. 

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>SetWindowsHookEx</b> can be used to inject a DLL into another process. A 32-bit DLL cannot be injected into a 64-bit process, and a 64-bit DLL cannot be injected into a 32-bit process. If an application requires the use of hooks in other processes, it is required that a 32-bit application call <b>SetWindowsHookEx</b> to inject a 32-bit DLL into 32-bit processes, and a 64-bit application call <b>SetWindowsHookEx</b> to inject a 64-bit DLL into 64-bit processes. The 32-bit and 64-bit DLLs must have different names.
		

Because hooks run in the context of an application, they must match the "bitness" of the application. If a 32-bit application installs a global hook on 64-bit Windows, the 32-bit hook is injected into each 32-bit process (the usual security boundaries apply). In a 64-bit process, the threads are still marked as "hooked." However, because a 32-bit application must run the hook code, the system executes the hook in the hooking app's context; specifically, on the thread that called <b>SetWindowsHookEx</b>. This means that the hooking application must continue to pump messages or it might block the normal functioning of the 64-bit processes.
 


If a 64-bit application installs a global hook on 64-bit Windows, the 64-bit hook is injected into each 64-bit process, while all 32-bit processes use a callback to the hooking application.
 


To hook all applications on the desktop of a 64-bit Windows installation, install a 32-bit global hook and a 64-bit global hook, each from appropriate processes, and be sure to keep pumping messages in the hooking application to avoid blocking normal functioning. If you already have a 32-bit global hooking application and it doesn't need to run in each application's context, you may not need to create a 64-bit version.


An error may occur if the <i>hMod</i> parameter is <b>NULL</b> and the <i>dwThreadId</i> parameter is zero or specifies the identifier of a thread created by another process. 

Calling the <a href="https://msdn.microsoft.com/2f734ea7-7724-46be-99a0-2bfa27b2ed99">CallNextHookEx</a> function to chain to the next hook procedure is optional, but it is highly recommended; otherwise, other applications that have installed hooks will not receive hook notifications and may behave incorrectly as a result. You should call <b>CallNextHookEx</b> unless you absolutely need to prevent the notification from being seen by other applications. 

Before terminating, an application must call the <a href="https://msdn.microsoft.com/0266fc5f-f62f-4bad-99b9-7cd16edb07de">UnhookWindowsHookEx</a> function to free system resources associated with the hook. 

The scope of a hook depends on the hook type. Some hooks can be set only with global scope; others can also be set for only a specific thread, as shown in the following table. 

<table class="clsStd">
<tr>
<th>Hook</th>
<th>Scope</th>
</tr>
<tr>
<td><b>WH_CALLWNDPROC</b></td>
<td>Thread or global</td>
</tr>
<tr>
<td><b>WH_CALLWNDPROCRET</b></td>
<td>Thread or global</td>
</tr>
<tr>
<td><b>WH_CBT</b></td>
<td>Thread or global</td>
</tr>
<tr>
<td><b>WH_DEBUG</b></td>
<td>Thread or global</td>
</tr>
<tr>
<td><b>WH_FOREGROUNDIDLE</b></td>
<td>Thread or global</td>
</tr>
<tr>
<td><b>WH_GETMESSAGE</b></td>
<td>Thread or global</td>
</tr>
<tr>
<td><b>WH_JOURNALPLAYBACK</b></td>
<td>Global only</td>
</tr>
<tr>
<td><b>WH_JOURNALRECORD</b></td>
<td>Global only</td>
</tr>
<tr>
<td><b>WH_KEYBOARD</b></td>
<td>Thread or global</td>
</tr>
<tr>
<td><b>WH_KEYBOARD_LL</b></td>
<td>Global only</td>
</tr>
<tr>
<td><b>WH_MOUSE</b></td>
<td>Thread or global</td>
</tr>
<tr>
<td><b>WH_MOUSE_LL</b></td>
<td>Global only</td>
</tr>
<tr>
<td><b>WH_MSGFILTER</b></td>
<td>Thread or global</td>
</tr>
<tr>
<td><b>WH_SHELL</b></td>
<td>Thread or global</td>
</tr>
<tr>
<td><b>WH_SYSMSGFILTER</b></td>
<td>Global only</td>
</tr>
</table>
 

For a specified hook type, thread hooks are called first, then global hooks. Be aware that the WH_MOUSE, WH_KEYBOARD, WH_JOURNAL*, WH_SHELL, and low-level hooks can be called on the thread that installed the hook rather than the thread processing the hook. For these hooks, it is possible that both the 32-bit and 64-bit hooks will be called if a 32-bit hook is ahead of a 64-bit hook in the hook chain.

The global hooks are a shared resource, and installing one affects all applications in the same desktop as the calling thread. All global hook functions must be in libraries. Global hooks should be restricted to special-purpose applications or to use as a development aid during application debugging. Libraries that no longer need a hook should remove its hook procedure. 

<b>Windows Store app development</b> If dwThreadId is zero, then window hook DLLs are not loaded in-process for the Windows Store app processes and the Windows Runtime broker process unless they are installed by either UIAccess processes (accessibility tools). The notification is delivered on the installer's thread for these hooks:

<ul>
<li>WH_JOURNALPLAYBACK</li>
<li>WH_JOURNALRECORD

</li>
<li>WH_KEYBOARD

</li>
<li>WH_KEYBOARD_LL

</li>
<li>WH_MOUSE

</li>
<li>WH_MOUSE_LL

</li>
</ul>
This behavior is similar to what happens when there is an architecture mismatch between the hook DLL and the target application process, for example, when the hook DLL is 32-bit and the application process 64-bit. 


#### Examples

For an example, see <a href="using_hooks.htm">Installing and Releasing Hook Procedures</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/26c48395-f0b8-4c03-bf65-d76cdf0117d6">CBTProc</a>



<a href="https://msdn.microsoft.com/2f734ea7-7724-46be-99a0-2bfa27b2ed99">CallNextHookEx</a>



<a href="https://msdn.microsoft.com/25df5ac2-f007-4683-ba89-537dc7a3c15e">CallWndProc</a>



<a href="https://msdn.microsoft.com/4e666fae-add5-4ea5-a314-e034f894d493">CallWndRetProc</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d9d446a1-1337-4efa-bb33-9e5b762476f8">DebugProc</a>



<a href="https://msdn.microsoft.com/de6f5c7b-df4f-4b63-ac46-236c332de2a3">ForegroundIdleProc</a>



<a href="https://msdn.microsoft.com/3d6a61eb-6c1d-4222-a627-c129822312b9">GetMsgProc</a>



<a href="https://msdn.microsoft.com/987095d7-059f-4eae-925d-6723ab6d524c">Hooks</a>



<a href="https://msdn.microsoft.com/ee7cfc0e-c04e-4f1c-bf03-e6ad770d4659">JournalPlaybackProc</a>



<a href="https://msdn.microsoft.com/377cdb26-563b-4014-ac52-ef0c441e94b5">JournalRecordProc</a>



<a href="https://msdn.microsoft.com/3fdcc0b4-013a-48e3-9a01-bf34953daddc">KeyboardProc</a>



<a href="https://msdn.microsoft.com/9d66accd-04cd-4839-b826-1c85dfb3b24e">LowLevelKeyboardProc</a>



<a href="https://msdn.microsoft.com/a0922155-22e5-410a-b64e-f87690de8a17">LowLevelMouseProc</a>



<a href="https://msdn.microsoft.com/20f8511d-8160-4565-99b3-d373501b1bd1">MessageProc</a>



<a href="https://msdn.microsoft.com/4fc1d81d-ee12-4ee4-b29c-2450b92b83b5">MouseProc</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/4c21e0d8-2529-4b04-ad45-762ca7f1e5ef">ShellProc</a>



<a href="https://msdn.microsoft.com/5ed3a4f0-8b7e-4896-b8d4-b5f071de895d">SysMsgProc</a>



<a href="https://msdn.microsoft.com/0266fc5f-f62f-4bad-99b9-7cd16edb07de">UnhookWindowsHookEx</a>
 

 

