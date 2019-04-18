---
UID: NF:debugapi.ContinueDebugEvent
title: ContinueDebugEvent function (debugapi.h)
author: windows-sdk-content
description: Enables a debugger to continue a thread that previously reported a debugging event.
old-location: base\continuedebugevent.htm
tech.root: Debug
ms.assetid: d15847d9-7947-4653-b3a2-3da1d1dd7078
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ContinueDebugEvent, ContinueDebugEvent function, DBG_CONTINUE, DBG_EXCEPTION_NOT_HANDLED, DBG_REPLY_LATER, _win32_continuedebugevent, base.continuedebugevent, debugapi/ContinueDebugEvent
ms.topic: function
req.header: debugapi.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-debug-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Debug-L1-1-2.dll
api_name:
 - ContinueDebugEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ContinueDebugEvent function


## -description


Enables a debugger to continue a thread that previously reported a debugging event.


## -parameters




### -param dwProcessId [in]

The process identifier  of the process to continue.


### -param dwThreadId [in]

The thread identifier of the thread to continue. The combination of process identifier and thread identifier must identify a thread that has previously reported a debugging event.


### -param dwContinueStatus [in]

The options to continue the thread that reported the debugging event. 




<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DBG_CONTINUE"></a><a id="dbg_continue"></a><dl>
<dt><b>DBG_CONTINUE</b></dt>
<dt>0x00010002L</dt>
</dl>
</td>
<td width="60%">
If the thread specified by the <i>dwThreadId</i> parameter previously reported an EXCEPTION_DEBUG_EVENT debugging event, the function stops all exception processing and continues the thread and the exception is marked as handled. For any other debugging event, this flag simply continues the thread.

</td>
</tr>
<tr>
<td width="40%"><a id="DBG_EXCEPTION_NOT_HANDLED"></a><a id="dbg_exception_not_handled"></a><dl>
<dt><b>DBG_EXCEPTION_NOT_HANDLED</b></dt>
<dt>0x80010001L</dt>
</dl>
</td>
<td width="60%">
If the thread specified by <i>dwThreadId</i> previously reported an EXCEPTION_DEBUG_EVENT debugging event, the function continues exception processing. If this is a first-chance exception event, the search and dispatch logic of the structured exception handler is used; otherwise, the process is terminated. For any other debugging event, this flag simply continues the thread.

</td>
</tr>
<tr>
<td width="40%"><a id="DBG_REPLY_LATER"></a><a id="dbg_reply_later"></a><dl>
<dt><b>DBG_REPLY_LATER</b></dt>
<dt>0x40010001L</dt>
</dl>
</td>
<td width="60%">
Supported in Windows 10, version 1507 or above, this flag causes <i>dwThreadId</i> to replay the existing breaking event after the target continues. By calling the <a href="https://msdn.microsoft.com/1332abcb-3356-4890-a03c-843358c1a3ce">SuspendThread</a> API against <i>dwThreadId</i>, a debugger can resume other threads in the process and later return to the breaking.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Only the thread that created <i>dwProcessId</i> with the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function can call 
<b>ContinueDebugEvent</b>.

After the 
<b>ContinueDebugEvent</b> function succeeds, the specified thread continues. Depending on the debugging event previously reported by the thread, different actions occur. If the continued thread previously reported an EXIT_THREAD_DEBUG_EVENT debugging event, 
<b>ContinueDebugEvent</b> closes the handle the debugger has to the thread. If the continued thread previously reported an EXIT_PROCESS_DEBUG_EVENT debugging event, 
<b>ContinueDebugEvent</b> closes the handles the debugger has to the process and to the thread.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/5a45854e-2711-49d5-982b-6b85248ec632">Writing the Debugger's Main Loop</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/43ca51f1-ba73-4031-96c3-5815311ce6f6">Debugging Events</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>
 

 

