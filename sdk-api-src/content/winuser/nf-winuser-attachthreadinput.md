---
UID: NF:winuser.AttachThreadInput
title: AttachThreadInput function (winuser.h)
description: Attaches or detaches the input processing mechanism of one thread to that of another thread.
helpviewer_keywords: ["AttachThreadInput","AttachThreadInput function","_win32_attachthreadinput","base.attachthreadinput","winuser/AttachThreadInput"]
old-location: base\attachthreadinput.htm
tech.root: backup
ms.assetid: 0c343fab-56ae-4c70-a79e-0c5f827158a3
ms.date: 12/05/2018
ms.keywords: AttachThreadInput, AttachThreadInput function, _win32_attachthreadinput, base.attachthreadinput, winuser/AttachThreadInput
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - AttachThreadInput
 - winuser/AttachThreadInput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - AttachThreadInput
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# AttachThreadInput function


## -description

Attaches or detaches the input processing mechanism of one thread to that of another thread.

## -parameters

### -param idAttach [in]

The identifier of the thread to be attached to another thread. The thread to be attached cannot be a system thread.

### -param idAttachTo [in]

The identifier of the thread to which <i>idAttach</i> will be attached. This thread cannot be a system thread. 




A thread cannot attach to itself. Therefore, <i>idAttachTo</i> cannot equal <i>idAttach</i>.

### -param fAttach [in]

If this parameter is <b>TRUE</b>, the two threads are attached. If the parameter is <b>FALSE</b>, the threads are detached.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<b>Windows Server 2003 and Windows XP:  </b>There is no extended error information; do not call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. This behavior changed as of Windows Vista.

## -remarks

By using the <b>AttachThreadInput</b> function, a thread can share its input states (such as keyboard states and the current focus window) with another thread. Keyboard and mouse events received by both threads are processed in the order they were received until the threads are detached by calling <b>AttachThreadInput</b> a second time and specifying <b>FALSE</b> for the <i>fAttach</i> parameter.

The 
<b>AttachThreadInput</b> function fails if either of the specified threads does not have a message queue. The system creates a thread's message queue when the thread makes its first call to one of the USER or GDI functions. The 
<b>AttachThreadInput</b> function also fails if a journal record hook is installed. Journal record hooks attach all input queues together.

Note that key state, which can be ascertained by calls to the 
<a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a> or 
<a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a> function, is reset after a call to 
<b>AttachThreadInput</b>. You cannot attach a thread to a thread in another <a href="/windows/desktop/winstation/desktops">desktop</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowthreadprocessid">GetWindowThreadProcessId</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-setfocus">SetFocus</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>
