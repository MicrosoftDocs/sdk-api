---
UID: NF:handleapi.DuplicateHandle
title: DuplicateHandle function (handleapi.h)
description: Duplicates an object handle.
helpviewer_keywords: ["DUPLICATE_CLOSE_SOURCE","DUPLICATE_SAME_ACCESS","DuplicateHandle","DuplicateHandle function","_win32_duplicatehandle","base.duplicatehandle","handleapi/DuplicateHandle"]
old-location: base\duplicatehandle.htm
tech.root: winprog
ms.assetid: 9c8da574-5bda-49f1-a6b6-c026639d6504
ms.date: 12/05/2018
ms.keywords: DUPLICATE_CLOSE_SOURCE, DUPLICATE_SAME_ACCESS, DuplicateHandle, DuplicateHandle function, _win32_duplicatehandle, base.duplicatehandle, handleapi/DuplicateHandle
req.header: handleapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - DuplicateHandle
 - handleapi/DuplicateHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-handle-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - DuplicateHandle
---

# DuplicateHandle function


## -description

Duplicates an object handle.

## -parameters

### -param hSourceProcessHandle [in]

A handle to the process with the handle to be duplicated. 




The handle must have the PROCESS_DUP_HANDLE access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param hSourceHandle [in]

The handle to be duplicated. This is an open object handle that is valid in the context of the source process. For a list of objects whose handles can be duplicated, see the following Remarks section.

If <i>hSourceHandle</i> is a pseudo handle returned by <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> or <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthread">GetCurrentThread</a>, <i>hSourceProcessHandle</i> should be a handle to the process calling <b>DuplicateHandle</b>.

### -param hTargetProcessHandle [in]

A handle to the process that is to receive the duplicated handle. The handle must have the PROCESS_DUP_HANDLE access right.

This parameter is optional and can be specified as NULL if the **DUPLICATE_CLOSE_SOURCE** flag is set in _Options_.

### -param lpTargetHandle [out]

A pointer to a variable that receives the duplicate handle. This handle value is valid in the context of the target process. 

If <i>hSourceHandle</i> is a pseudo handle returned by <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> or <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthread">GetCurrentThread</a>, <b>DuplicateHandle</b> converts it to a real handle to a process or thread, respectively.

If <i>lpTargetHandle</i> is <b>NULL</b>, the function duplicates the handle, but does not return the duplicate handle value to the caller. This behavior exists only for backward compatibility with previous versions of this function. You should not use this feature, as you will lose system resources until the target process terminates.

This parameter is ignored if _hTargetProcessHandle_ is **NULL**.

### -param dwDesiredAccess [in]

The access requested for the new handle. For the flags that can be specified for each object type, see the following Remarks section. 

This parameter is ignored if the <i>dwOptions</i> parameter specifies the DUPLICATE_SAME_ACCESS flag. Otherwise, the flags that can be specified depend on the type of object whose handle is to be duplicated.

This parameter is ignored if _hTargetProcessHandle_ is **NULL**.

### -param bInheritHandle [in]

A variable that indicates whether the handle is inheritable. If <b>TRUE</b>, the duplicate handle can be inherited by new processes created by the target process. If <b>FALSE</b>, the new handle cannot be inherited.

This parameter is ignored if _hTargetProcessHandle_ is **NULL**.

### -param dwOptions [in]

Optional actions. This parameter can be zero, or any combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DUPLICATE_CLOSE_SOURCE"></a><a id="duplicate_close_source"></a><dl>
<dt><b>DUPLICATE_CLOSE_SOURCE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Closes the source handle. This occurs regardless of any error status returned.

</td>
</tr>
<tr>
<td width="40%"><a id="DUPLICATE_SAME_ACCESS"></a><a id="duplicate_same_access"></a><dl>
<dt><b>DUPLICATE_SAME_ACCESS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Ignores the <i>dwDesiredAccess</i> parameter. The duplicate handle has the same access as the source handle.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The duplicate handle refers to the same object as the original handle. Therefore, any changes to the object are reflected through both handles. For example, if you duplicate a file handle, the current file position is always the same for both handles. For  file handles to have different file positions, use the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function to create file handles that share access to the same file.

<b>DuplicateHandle</b> can be called by either the source process or the target process (or a process that is both the source and target process). For example, a process can use 
<b>DuplicateHandle</b> to create a noninheritable duplicate of an inheritable handle, or a handle with different access than the original handle.

The source process uses the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> function to get a handle to itself. This handle is a pseudo handle, but <b>DuplicateHandle</b> converts it to a real process handle. To get the target process handle, it may be necessary to use some form of interprocess communication (for example, a named pipe or shared memory) to communicate the process identifier to the source process. The source process can use this identifier in the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a> function to obtain a handle to the target process.

If the process that calls 
<b>DuplicateHandle</b> is not also the target process, the source process must use interprocess communication to pass the value of the duplicate handle to the target process.

<b>DuplicateHandle</b> can be used to duplicate a handle between a 32-bit process and a 64-bit process. The resulting handle is appropriately sized to work in the target process. For more information, see <a href="/windows/desktop/WinProg64/process-interoperability">Process Interoperability</a>.

<b>DuplicateHandle</b> can duplicate handles to the following types of objects.

<table>
<tr>
<th>Object</th>
<th>Description</th>
</tr>
<tr>
<td>Access token</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>, or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> function.</td>
</tr>
<tr>
<td>Change notification</td>
<td>The handle is returned by the <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa">FindFirstChangeNotification</a> function.</td>
</tr>
<tr>
<td>Communications device</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.</td>
</tr>
<tr>
<td>Console input</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function when CONIN$ is specified, or by the 
<a href="/windows/console/getstdhandle">GetStdHandle</a> function when STD_INPUT_HANDLE is specified. Console handles can be duplicated for use only in the same process.</td>
</tr>
<tr>
<td>Console screen buffer</td>
<td>The handle is returned by the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function when CONOUT$ is specified, or by the <a href="/windows/console/getstdhandle">GetStdHandle</a> function when STD_OUTPUT_HANDLE is specified. Console handles can be duplicated for use only in the same process.</td>
</tr>
<tr>
<td>Desktop</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/winuser/nf-winuser-getthreaddesktop">GetThreadDesktop</a> function.</td>
</tr>
<tr>
<td>Event</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or 
<a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a> function.</td>
</tr>
<tr>
<td>File</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.</td>
</tr>
<tr>
<td>File mapping</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a> function.</td>
</tr>
<tr>
<td>Job</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/winbase/nf-winbase-createjobobjecta">CreateJobObject</a> function.</td>
</tr>
<tr>
<td>Mailslot</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/winbase/nf-winbase-createmailslota">CreateMailslot</a> function.</td>
</tr>
<tr>
<td>Mutex</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createmutexa">CreateMutex</a> or 
[OpenMutex](../synchapi/nf-synchapi-openmutexw.md) function.</td>
</tr>
<tr>
<td>Pipe</td>
<td>A named pipe handle is returned by the 
<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> or 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. An anonymous pipe handle is returned by the 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe">CreatePipe</a> function.</td>
</tr>
<tr>
<td>Process</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a>, or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a> function.</td>
</tr>
<tr>
<td>Registry key</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeya">RegCreateKey</a>, 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeya">RegOpenKey</a>, or 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function. Note that registry key handles returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regconnectregistrya">RegConnectRegistry</a> function cannot be used in a call to 
<b>DuplicateHandle</b>. </td>
</tr>
<tr>
<td>Semaphore</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/winbase/nf-winbase-createsemaphorea">CreateSemaphore</a> or 
<a href="/windows/win32/api/synchapi/nf-synchapi-opensemaphorew">OpenSemaphore</a> function.</td>
</tr>
<tr>
<td>Thread</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createremotethread">CreateRemoteThread</a>, or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthread">GetCurrentThread</a> function</td>
</tr>
<tr>
<td>Timer</td>
<td>The handle is returned by the 
<a href="/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw">CreateWaitableTimerW</a> or <a href="/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw">OpenWaitableTimerW</a> function.</td>
</tr>
<tr>
<td>Transaction</td>
<td>The handle is returned by the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.</td>
</tr>
<tr>
<td>Window station</td>
<td>The handle is returned by the 
<a href="/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation">GetProcessWindowStation</a> function.</td>
</tr>
</table>
 

You should not use 
<b>DuplicateHandle</b> to duplicate handles to the following objects:

<ul>
<li>I/O completion ports. No error is returned, but the duplicate handle cannot be used.</li>
<li>Sockets. No error is returned, but the duplicate handle may not be recognized by Winsock at the target process. Also, using <b>DuplicateHandle</b> interferes with internal reference counting on the underlying object. To duplicate a socket handle, use the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaduplicatesocketa">WSADuplicateSocket</a> function.</li>
<li>Pseudo-handles other than the ones returned by the <a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> or <a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread">GetCurrentThread</a> functions.</li>
</ul>
The <i>dwDesiredAccess</i> parameter specifies the new handle's access rights. All objects support the <a href="/windows/desktop/SecAuthZ/standard-access-rights">standard access rights</a>. Objects may also support additional access rights depending on the object type. For more information, see the following topics:

<ul>
<li>
<a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktop Security and Access Rights</a>
</li>
<li>
<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>
</li>
<li>
<a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File-Mapping Security and Access Rights</a>
</li>
<li>
<a href="/windows/desktop/ProcThread/job-object-security-and-access-rights">Job Object Security and Access Rights</a>
</li>
<li>
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>
</li>
<li>
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>
</li>
<li>
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>
</li>
<li>
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>
</li>
<li>
<a href="/windows/desktop/winstation/window-station-security-and-access-rights">Window-Station Security and Access Rights</a>
</li>
</ul>
In some cases, the new handle can have more access rights than the original handle. However, in other cases, 
<b>DuplicateHandle</b> cannot create a handle with more access rights than the original. For example, a file handle created with the GENERIC_READ access right cannot be duplicated so that it has both the GENERIC_READ and GENERIC_WRITE access right.

Normally the target process closes a duplicated handle when that process is finished using the handle. To close a duplicated handle from the source process,  call <b>DuplicateHandle</b> with the following parameters: 

<ul>
<li>Set <i>hSourceProcessHandle</i> to the target process from the <b>DuplicateHandle</b> call that created the handle.</li>
<li>Set <i>hSourceHandle</i> to the duplicated handle to close.</li>
<li>Set <i>hTargetProcessHandle</i> to <b>NULL</b>.</li>
<li>Set <i>dwOptions</i> to DUPLICATE_CLOSE_SOURCE.</li>
</ul>

#### Examples

The following example creates a mutex, duplicates a handle to the mutex, and passes it to another thread. Duplicating the handle ensures that the reference count is increased so that the mutex object will not be destroyed until both threads have closed the handle.


```cpp
#include <windows.h>

DWORD CALLBACK ThreadProc(PVOID pvParam);

int main()
{
    HANDLE hMutex = CreateMutex(NULL, FALSE, NULL);
    HANDLE hMutexDup, hThread;
    DWORD dwThreadId;

    DuplicateHandle(GetCurrentProcess(), 
                    hMutex, 
                    GetCurrentProcess(),
                    &hMutexDup, 
                    0,
                    FALSE,
                    DUPLICATE_SAME_ACCESS);

    hThread = CreateThread(NULL, 0, ThreadProc, 
        (LPVOID) hMutexDup, 0, &dwThreadId);

    // Perform work here, closing the handle when finished with the
    // mutex. If the reference count is zero, the object is destroyed.
    CloseHandle(hMutex);

    // Wait for the worker thread to terminate and clean up.
    WaitForSingleObject(hThread, INFINITE);
    CloseHandle(hThread);
    return 0;
}

DWORD CALLBACK ThreadProc(PVOID pvParam)
{
    HANDLE hMutex = (HANDLE)pvParam;

    // Perform work here, closing the handle when finished with the
    // mutex. If the reference count is zero, the object is destroyed.
    CloseHandle(hMutex);
    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/SysInfo/handle-inheritance">Handle Inheritance</a>



<a href="/windows/desktop/SysInfo/handle-and-object-functions">Handle and
		  Object Functions</a>
