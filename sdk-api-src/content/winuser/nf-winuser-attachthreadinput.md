---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<b>Windows Server 2003 and Windows XP:  </b>There is no extended error information; do not call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. This behavior changed as of Windows Vista.




## -remarks



Windows created in different threads typically process input independently of each other. That is, they have their own input states (focus, active, capture windows, key state, queue status, and so on), and their input processing is not synchronized with the input processing of other threads. By using the 
<b>AttachThreadInput</b> function, a thread can attach its input processing mechanism to another thread. Keyboard and mouse events received by both threads are processed by the  thread specified by the <i>idAttachTo</i> parameter until the threads are detached by calling <b>AttachThreadInput</b> a second time and specifying <b>FALSE</b> for the <i>fAttach</i> parameter. This also allows threads to share their input states, so they can call the <a href="_win32_setfocus_cpp">SetFocus</a> function to set the keyboard focus to a window of a different thread. This also allows threads to get key-state information. 

The 
<b>AttachThreadInput</b> function fails if either of the specified threads does not have a message queue. The system creates a thread's message queue when the thread makes its first call to one of the USER or GDI functions. The 
<b>AttachThreadInput</b> function also fails if a journal record hook is installed. Journal record hooks attach all input queues together.

Note that key state, which can be ascertained by calls to the 
<a href="_win32_getkeystate_cpp">GetKeyState</a> or 
<a href="_win32_getkeyboardstate_cpp">GetKeyboardState</a> function, is reset after a call to 
<b>AttachThreadInput</b>. You cannot attach a thread to a thread in another <a href="https://msdn.microsoft.com/library/windows/hardware/mt483735">desktop</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546542">GetCurrentThreadId</a>



<a href="_win32_getkeystate_cpp">GetKeyState</a>



<a href="_win32_getkeyboardstate_cpp">GetKeyboardState</a>



<a href="_win32_getwindowthreadprocessid_cpp">GetWindowThreadProcessId</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="_win32_setfocus_cpp">SetFocus</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

