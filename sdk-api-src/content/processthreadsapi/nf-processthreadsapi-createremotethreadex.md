---
UID: NF:processthreadsapi.CreateRemoteThreadEx
title: CreateRemoteThreadEx function (processthreadsapi.h)
description: Creates a thread that runs in the virtual address space of another process and optionally specifies extended attributes such as processor group affinity.
helpviewer_keywords: ["CREATE_SUSPENDED","CreateRemoteThreadEx","CreateRemoteThreadEx function","STACK_SIZE_PARAM_IS_A_RESERVATION","base.createremotethreadex","processthreadsapi/CreateRemoteThreadEx","winbase/CreateRemoteThreadEx"]
old-location: base\createremotethreadex.htm
tech.root: processthreadsapi
ms.assetid: 9c2d9e20-7614-4010-9b8b-4f0e9bc2e6fe
ms.date: 12/05/2018
ms.keywords: CREATE_SUSPENDED, CreateRemoteThreadEx, CreateRemoteThreadEx function, STACK_SIZE_PARAM_IS_A_RESERVATION, base.createremotethreadex, processthreadsapi/CreateRemoteThreadEx, winbase/CreateRemoteThreadEx
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateRemoteThreadEx
 - processthreadsapi/CreateRemoteThreadEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - CreateRemoteThreadEx
---

# CreateRemoteThreadEx function


## -description

Creates a thread that runs in the virtual address space of another process and optionally specifies extended attributes such as processor group affinity.

## -parameters

### -param hProcess [in]

A handle to the process in which the thread is to be created. The handle must have the PROCESS_CREATE_THREAD, PROCESS_QUERY_INFORMATION, PROCESS_VM_OPERATION, PROCESS_VM_WRITE, and PROCESS_VM_READ access rights. In Windows 10, version 1607, your code must obtain these access rights for the new handle. However, starting in Windows 10, version 1703, if the new handle is entitled to these access rights, the system obtains them for you. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param lpThreadAttributes [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that specifies a security descriptor for the new thread and determines whether child processes can inherit the returned handle. If <i>lpThreadAttributes</i> is NULL, the thread gets a default security descriptor and the handle cannot be inherited. The access control lists (ACL) in the default security descriptor for a thread come from the primary token of the creator.

### -param dwStackSize [in]

The initial size of the stack, in bytes. The system rounds this value to the nearest page. If this parameter is 0 (zero), the new thread uses the default size for the executable. For more information, see 
<a href="/windows/desktop/ProcThread/thread-stack-size">Thread Stack Size</a>.

### -param lpStartAddress [in]

A pointer to the application-defined function of type <b>LPTHREAD_START_ROUTINE</b> to be executed by the thread and represents the starting address of the thread in the remote process. The function must exist in the remote process. For more information, see 
<a href="/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)">ThreadProc</a>.

### -param lpParameter [in, optional]

A pointer to a variable to be passed to the thread function pointed to by <i>lpStartAddress</i>. This parameter can be NULL.

### -param dwCreationFlags [in]

The flags that control the creation of the thread.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The thread runs immediately after creation.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_SUSPENDED"></a><a id="create_suspended"></a><dl>
<dt><b>CREATE_SUSPENDED</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The thread is created in a suspended state and does not run until the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-resumethread">ResumeThread</a> function is called.

</td>
</tr>
<tr>
<td width="40%"><a id="STACK_SIZE_PARAM_IS_A_RESERVATION"></a><a id="stack_size_param_is_a_reservation"></a><dl>
<dt><b>STACK_SIZE_PARAM_IS_A_RESERVATION</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The <i>dwStackSize</i> parameter specifies the initial reserve size of the stack. If this flag is not specified, <i>dwStackSize</i> specifies the commit size.

</td>
</tr>
</table>

### -param lpAttributeList [in, optional]

An attribute list that contains additional parameters for the new thread. This list is created by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist">InitializeProcThreadAttributeList</a> function.

### -param lpThreadId [out, optional]

A pointer to a variable that receives the thread identifier. 




If this parameter is NULL, the thread identifier is not returned.

## -returns

If the function succeeds, the return value is a handle to the new thread.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>CreateRemoteThreadEx</b> function causes a new thread of execution to begin in the address space of the specified process. The thread has access to all objects that the process opens. The <i>lpAttribute</i> parameter can be used to specify extended attributes such as processor group affinity for the new thread. If <i>lpAttribute</i> is NULL, the function's behavior is the same as  <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createremotethread">CreateRemoteThread</a>.  

Prior to Windows 8, Terminal Services isolates each terminal session by design. Therefore, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createremotethread">CreateRemoteThread</a> fails if the target process is in a different session than the calling process.

The new thread handle is created with full access to the new thread. If a security descriptor is not provided, the handle may be used in any function that requires a thread object handle. When a security descriptor is provided, an access check is performed on all subsequent uses of the handle before access is granted. If the access check denies access, the requesting process cannot use the handle to gain access to the thread.

 If the thread is created in a runnable state (that is, if the CREATE_SUSPENDED flag is not used), the thread can start running before <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a> returns and, in particular, before  the caller receives the handle and identifier of the created thread.

The thread is created with a thread priority of THREAD_PRIORITY_NORMAL. To get and set the priority value of a thread, use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadpriority">GetThreadPriority</a> and 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority">SetThreadPriority</a> functions.

When a thread terminates, the thread object attains a signaled state, which satisfies the threads that are waiting for the object.

The thread object remains in the system until the thread has terminated and all handles to it are closed through a call to 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

The 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createremotethread">CreateRemoteThread</a> functions, and a process that is starting (as the result of a 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> call) are serialized between each other within a process. Only one of these events occurs in an address space at a time. This means the following restrictions hold:

<ul>
<li>During process startup and DLL initialization routines, new threads can be created, but they do not begin execution until DLL initialization is done for the process.</li>
<li>Only one thread in a process can be in a DLL initialization or detach routine at a time.</li>
<li>
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a> returns after all threads have completed their DLL initialization or detach routines. </li>
</ul>
A common use of this function is to inject a thread into a process that is being debugged to issue a break. However, this use is not recommended, because the extra thread is confusing to the person debugging the application and there are several side effects to using this technique:

<ul>
<li>It converts single-threaded applications into multithreaded applications.</li>
<li>It changes the timing and memory layout of the process.</li>
<li>It results in a call to the entry point of each DLL in the process.</li>
</ul>
Another common use of this function is to inject a thread into a process to query heap or other process information. This can cause the same side effects mentioned in the previous paragraph. Also, the application can deadlock if the thread attempts to obtain ownership of locks that another thread is using.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createremotethread">CreateRemoteThread</a>