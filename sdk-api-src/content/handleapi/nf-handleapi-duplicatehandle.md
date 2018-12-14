---
UID: NF:handleapi.DuplicateHandle
title: DuplicateHandle function
author: windows-sdk-content
description: Duplicates an object handle.
old-location: base\duplicatehandle.htm
tech.root: sysinfo
ms.assetid: 9c8da574-5bda-49f1-a6b6-c026639d6504
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DUPLICATE_CLOSE_SOURCE, DUPLICATE_SAME_ACCESS, DuplicateHandle, DuplicateHandle function, _win32_duplicatehandle, base.duplicatehandle, handleapi/DuplicateHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DuplicateHandle function


## -description


Duplicates an object handle.


## -parameters




### -param hSourceProcessHandle [in]

A handle to the process with the handle to be duplicated. 




The handle must have the PROCESS_DUP_HANDLE access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param hSourceHandle [in]

The handle to be duplicated. This is an open object handle that is valid in the context of the source process. For a list of objects whose handles can be duplicated, see the following Remarks section.


### -param hTargetProcessHandle [in]

A handle to the process that is to receive the duplicated handle. The handle must have the PROCESS_DUP_HANDLE access right.


### -param lpTargetHandle [out]

A pointer to a variable that receives the duplicate handle. This handle value is valid in the context of the target process. 




If <i>hSourceHandle</i> is a pseudo handle returned by <a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a> or <a href="https://msdn.microsoft.com/91a11552-66c1-42bd-b837-8a7685977bc9">GetCurrentThread</a>, <b>DuplicateHandle</b> converts it to a real  handle to a process or thread, respectively.

If <i>lpTargetHandle</i> is <b>NULL</b>, the function duplicates the handle, but does not return the duplicate handle value to the caller. This behavior exists only for backward compatibility with previous versions of this function. You should not use this feature, as you will lose system resources until the target process terminates.


### -param dwDesiredAccess [in]

The access requested for the new handle. For the flags that can be specified for each object type, see the following Remarks section. 




This parameter is ignored if the <i>dwOptions</i> parameter specifies the DUPLICATE_SAME_ACCESS flag. Otherwise, the flags that can be specified depend on the type of object whose handle is to be duplicated.


### -param bInheritHandle [in]

A variable that indicates whether the handle is inheritable. If <b>TRUE</b>, the duplicate handle can be inherited by new processes created by the target process. If <b>FALSE</b>, the new handle cannot be inherited.


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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The duplicate handle refers to the same object as the original handle. Therefore, any changes to the object are reflected through both handles. For example, if you duplicate a file handle, the current file position is always the same for both handles. For  file handles to have different file positions, use the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function to create file handles that share access to the same file.

<b>DuplicateHandle</b> can be called by either the source process or the target process (or a process that is both the source and target process). For example, a process can use 
<b>DuplicateHandle</b> to create a noninheritable duplicate of an inheritable handle, or a handle with different access than the original handle.

The source process uses the 
<a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a> function to get a handle to itself. This handle is a pseudo handle, but <b>DuplicateHandle</b> converts it to a real process handle. To get the target process handle, it may be necessary to use some form of interprocess communication (for example, a named pipe or shared memory) to communicate the process identifier to the source process. The source process can use this identifier in the 
<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a> function to obtain a handle to the target process.

If the process that calls 
<b>DuplicateHandle</b> is not also the target process, the source process must use interprocess communication to pass the value of the duplicate handle to the target process.

<b>DuplicateHandle</b> can be used to duplicate a handle between a 32-bit process and a 64-bit process. The resulting handle is appropriately sized to work in the target process. For more information, see <a href="https://msdn.microsoft.com/a573f26c-7577-4ff0-b314-ae0a33274738">Process Interoperability</a>.

<b>DuplicateHandle</b> can duplicate handles to the following types of objects.

<table>
<tr>
<th>Object</th>
<th>Description</th>
</tr>
<tr>
<td>Access token</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>, 
<a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>, 
<a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a>, 
<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>, or 
<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a> function.</td>
</tr>
<tr>
<td>Change notification</td>
<td>The handle is returned by the <a href="https://msdn.microsoft.com/en-us/library/Aa364417(v=VS.85).aspx">FindFirstChangeNotification</a> function.</td>
</tr>
<tr>
<td>Communications device</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function.</td>
</tr>
<tr>
<td>Console input</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function when CONIN$ is specified, or by the 
<a href="https://msdn.microsoft.com/library/ms683231(v=VS.85).aspx">GetStdHandle</a> function when STD_INPUT_HANDLE is specified. Console handles can be duplicated for use only in the same process.</td>
</tr>
<tr>
<td>Console screen buffer</td>
<td>The handle is returned by the <a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function when CONOUT$ is specified, or by the <a href="https://msdn.microsoft.com/library/ms683231(v=VS.85).aspx">GetStdHandle</a> function when STD_OUTPUT_HANDLE is specified. Console handles can be duplicated for use only in the same process.</td>
</tr>
<tr>
<td>Desktop</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/51eec935-43c7-495b-b1fc-2bd5ba1e0090">GetThreadDesktop</a> function.</td>
</tr>
<tr>
<td>Event</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> or 
<a href="https://msdn.microsoft.com/46741024-ace3-44d6-b8a6-5621ad121a1a">OpenEvent</a> function.</td>
</tr>
<tr>
<td>File</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function.</td>
</tr>
<tr>
<td>File mapping</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/d3302183-76a0-47ec-874f-1173db353dfe">CreateFileMapping</a> function.</td>
</tr>
<tr>
<td>Job</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/ca6a044f-67ed-4a9c-9aeb-69dd77652854">CreateJobObject</a> function.</td>
</tr>
<tr>
<td>Mailslot</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/a2e8199f-4d00-4315-9562-ff30f4fafcb7">CreateMailslot</a> function.</td>
</tr>
<tr>
<td>Mutex</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a> or 
<a href="https://msdn.microsoft.com/en-us/library/ms684315(v=VS.85).aspx">OpenMutex</a> function.</td>
</tr>
<tr>
<td>Pipe</td>
<td>A named pipe handle is returned by the 
<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a> or 
<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function. An anonymous pipe handle is returned by the 
<a href="https://msdn.microsoft.com/a2d2fee8-c174-49d3-9e5a-2ce3bb763932">CreatePipe</a> function.</td>
</tr>
<tr>
<td>Process</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>, 
<a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a>, or 
<a href="https://msdn.microsoft.com/8f695c38-19c4-49e4-97de-8b64ea536cb1">OpenProcess</a> function.</td>
</tr>
<tr>
<td>Registry key</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/cb4d30f4-e288-41e8-86e0-807c313db53d">RegCreateKey</a>, 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>, 
<a href="https://msdn.microsoft.com/bad0a0f8-1889-4eff-98be-084c95d69f3b">RegOpenKey</a>, or 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function. Note that registry key handles returned by the 
<a href="https://msdn.microsoft.com/d7fb41cc-4855-4ad7-879c-b1ac85ac5803">RegConnectRegistry</a> function cannot be used in a call to 
<b>DuplicateHandle</b>. </td>
</tr>
<tr>
<td>Semaphore</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/2e55d67b-99de-4f10-8637-00d9d62e4460">CreateSemaphore</a> or 
<a href="https://msdn.microsoft.com/en-us/library/ms684326(v=VS.85).aspx">OpenSemaphore</a> function.</td>
</tr>
<tr>
<td>Thread</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>, 
<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a>, 
<a href="https://msdn.microsoft.com/f5257f78-b20f-4db5-b63e-3bb4e41a4b19">CreateRemoteThread</a>, or 
<a href="https://msdn.microsoft.com/91a11552-66c1-42bd-b837-8a7685977bc9">GetCurrentThread</a> function</td>
</tr>
<tr>
<td>Timer</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/en-us/library/ms682492(v=VS.85).aspx">CreateWaitableTimer</a> or 
<a href="https://msdn.microsoft.com/en-us/library/ms684337(v=VS.85).aspx">OpenWaitableTimer</a> function.</td>
</tr>
<tr>
<td>Transaction</td>
<td>The handle is returned by the <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.</td>
</tr>
<tr>
<td>Window station</td>
<td>The handle is returned by the 
<a href="https://msdn.microsoft.com/f8929122-d277-4260-b2a7-5e76eb3ca876">GetProcessWindowStation</a> function.</td>
</tr>
</table>
 

You should not use 
<b>DuplicateHandle</b> to duplicate handles to the following objects:

<ul>
<li>I/O completion ports. No error is returned, but the duplicate handle cannot be used.</li>
<li>Sockets. No error is returned, but the duplicate handle may not be recognized by Winsock at the target process. Also, using <b>DuplicateHandle</b> interferes with internal reference counting on the underlying object. To duplicate a socket handle, use the <a href="https://msdn.microsoft.com/d4028461-bfa6-4074-9460-5d1371790d41">WSADuplicateSocket</a> function.</li>
</ul>
The <i>dwDesiredAccess</i> parameter specifies the new handle's access rights. All objects support the <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">standard access rights</a>. Objects may also support additional access rights depending on the object type. For more information, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/6512d128-3b0c-4ba7-8709-2fd225389a40">Desktop Security and Access Rights</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa364399(v=VS.85).aspx">File Security and Access Rights</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8bbf7c98-ff83-4ed9-8b82-f08dcd31295c">File-Mapping Security and Access Rights</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8d212292-f087-41e4-884e-cec4423dac49">Job Object Security and Access Rights</a>
</li>
<li>
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>
</li>
<li>
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>
</li>
<li>
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>
</li>
<li>
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b132da61-26b7-4457-9433-4894ca0e640a">Window-Station Security and Access Rights</a>
</li>
</ul>
In some cases, the new handle can have more access rights than the original handle. However, in other cases, 
<b>DuplicateHandle</b> cannot create a handle with more access rights than the original. For example, a file handle created with the GENERIC_READ access right cannot be duplicated so that it has both the GENERIC_READ and GENERIC_WRITE access right.

Normally the target process closes a duplicated handle when that process is finished using the handle. To close a duplicated handle from the source process,  call <b>DuplicateHandle</b> with the following parameters: 

<ul>
<li>Set <i>hSourceProcessHandle</i> to the target process from the <b>DuplicateHandle</b> call that created the handle.</li>
<li>Set <i>hSourceHandle</i> to the duplicated handle to close.</li>
<li>Set <i>lpTargetHandle</i> to <b>NULL</b>.</li>
<li>Set <i>dwOptions</i> to DUPLICATE_CLOSE_SOURCE.</li>
</ul>

#### Examples

The following example creates a mutex, duplicates a handle to the mutex, and passes it to another thread. Duplicating the handle ensures that the reference count is increased so that the mutex object will not be destroyed until both threads have closed the handle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;

DWORD CALLBACK ThreadProc(PVOID pvParam);

int main()
{
    HANDLE hMutex = CreateMutex(NULL, FALSE, NULL);
    HANDLE hMutexDup, hThread;
    DWORD dwThreadId;

    DuplicateHandle(GetCurrentProcess(), 
                    hMutex, 
                    GetCurrentProcess(),
                    &amp;hMutexDup, 
                    0,
                    FALSE,
                    DUPLICATE_SAME_ACCESS);

    hThread = CreateThread(NULL, 0, ThreadProc, 
        (LPVOID) hMutexDup, 0, &amp;dwThreadId);

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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/957cd369-bebf-4e04-9f7e-a936e2e97887">Handle Inheritance</a>



<a href="https://msdn.microsoft.com/b4769e19-7478-4919-a9d2-8086ece6da70">Handle and
		  Object Functions</a>
 

 

