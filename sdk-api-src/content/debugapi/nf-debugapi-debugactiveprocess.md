---
UID: NF:debugapi.DebugActiveProcess
title: DebugActiveProcess function (debugapi.h)
author: windows-sdk-content
description: Enables a debugger to attach to an active process and debug it.
old-location: base\debugactiveprocess.htm
tech.root: Debug
ms.assetid: 306a5b28-658a-4dab-a516-c638b73f4a77
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DebugActiveProcess, DebugActiveProcess function, _win32_debugactiveprocess, base.debugactiveprocess, debugapi/DebugActiveProcess
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
 - DebugActiveProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DebugActiveProcess function


## -description


Enables a debugger to attach to an active process and debug it.


## -parameters




### -param dwProcessId [in]

The identifier for the process to be debugged. The debugger is granted debugging access to the process as 
      if it created the process with the <b>DEBUG_ONLY_THIS_PROCESS</b> flag. For more information, 
      see the Remarks section of this topic.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To stop debugging the process, you must exit the process or call the 
    <a href="https://msdn.microsoft.com/29d1a6d1-0c10-43c1-bef1-b063f07b16a4">DebugActiveProcessStop</a> function. Exiting the 
    debugger also exits the process unless you use the 
    <a href="https://msdn.microsoft.com/7ef44527-bde4-41f0-a470-d3f404c77ea9">DebugSetProcessKillOnExit</a> function.

The debugger must have appropriate access to the target process, and it must be able to open the process for 
    <b>PROCESS_ALL_ACCESS</b>. 
    <b>DebugActiveProcess</b> can fail if the target process 
    is created with a security descriptor that grants the debugger anything less than full access. If the debugging 
    process has the <b>SE_DEBUG_NAME</b> privilege granted and enabled, it can debug any 
    process.

After the system checks the process identifier and determines that a valid debugging attachment is being made, 
    the function returns <b>TRUE</b>. Then the debugger is expected to wait for debugging events by 
    using the <a href="https://msdn.microsoft.com/0d81a4ac-dd66-4648-9f3f-1f54aca84243">WaitForDebugEvent</a> function. The system 
    suspends all threads in the process, and sends the debugger events that represents the current state of the 
    process.

The system sends the debugger a single <b>CREATE_PROCESS_DEBUG_EVENT</b> debugging event 
    that represents the process specified by the <i>dwProcessId</i> parameter. The 
    <b>lpStartAddress</b> member of the 
    <a href="https://msdn.microsoft.com/4607aaff-bd05-46b5-86ed-abfffe6c2551">CREATE_PROCESS_DEBUG_INFO</a> structure is 
    <b>NULL</b>.

For each thread that is currently part of the process, the system sends a 
    <b>CREATE_THREAD_DEBUG_EVENT</b> debugging event. The <b>lpStartAddress</b> 
    member of the <a href="https://msdn.microsoft.com/daabd118-fa03-410e-af25-8655194902b0">CREATE_THREAD_DEBUG_INFO</a> 
    structure is <b>NULL</b>.

For each dynamic-link library (DLL) that is currently loaded into the address space of the target process, the 
    system sends a <b>LOAD_DLL_DEBUG_EVENT</b> debugging event. The system arranges for the first 
    thread in the process to execute a breakpoint instruction after it resumes. Continuing this thread causes it to 
    return to doing the same thing as before the debugger is attached.

After all of this is done, the system resumes all threads in the process. When the first thread in the process 
    resumes, it executes a breakpoint instruction that causes an <b>EXCEPTION_DEBUG_EVENT</b> 
    debugging event to be sent to the debugger. All future debugging events are sent to the debugger by using the 
    normal mechanism and rules.




## -see-also




<a href="https://msdn.microsoft.com/4607aaff-bd05-46b5-86ed-abfffe6c2551">CREATE_PROCESS_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/daabd118-fa03-410e-af25-8655194902b0">CREATE_THREAD_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/29d1a6d1-0c10-43c1-bef1-b063f07b16a4">DebugActiveProcessStop</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/2662411f-a69a-442b-a177-a27ea025bb01">Debugging a Running Process</a>



<a href="https://msdn.microsoft.com/0d81a4ac-dd66-4648-9f3f-1f54aca84243">WaitForDebugEvent</a>
 

 

