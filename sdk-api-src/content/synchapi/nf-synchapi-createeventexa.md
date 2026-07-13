---
UID: NF:synchapi.CreateEventExA
title: CreateEventExA function (synchapi.h)
description: Creates or opens a named or unnamed event object and returns a handle to the object. (ANSI)
helpviewer_keywords: ["CREATE_EVENT_INITIAL_SET", "CREATE_EVENT_MANUAL_RESET", "CreateEventExA", "synchapi/CreateEventExA"]
old-location: base\createeventex.htm
tech.root: base
ms.assetid: 402a721d-8338-4df1-ba0b-074f868a1731
ms.date: 12/05/2018
ms.keywords: CREATE_EVENT_INITIAL_SET, CREATE_EVENT_MANUAL_RESET, CreateEventEx, CreateEventEx function, CreateEventExA, CreateEventExW, base.createeventex, synchapi/CreateEventEx, synchapi/CreateEventExA, synchapi/CreateEventExW, winbase/CreateEventEx, winbase/CreateEventExA, winbase/CreateEventExW
req.header: synchapi.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateEventExW (Unicode) and CreateEventExA (ANSI)
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
 - CreateEventExA
 - synchapi/CreateEventExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CreateEventEx
 - CreateEventExA
 - CreateEventExW
---

# CreateEventExA function


## -description

Creates or opens a named or unnamed event object and returns a handle to the object.

## -parameters

### -param lpEventAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure. If 
      <i>lpEventAttributes</i> is <b>NULL</b>, the event handle cannot be inherited by child processes.

The <b>lpSecurityDescriptor</b> member of the structure specifies a 
       <a href="/windows/desktop/SecAuthZ/security-descriptors">security descriptor</a> for the new 
       event. If <i>lpEventAttributes</i> is <b>NULL</b>, the event gets a default security descriptor. 
       The ACLs in the default security descriptor for an event come from the primary or impersonation token of the creator.

### -param lpName [in, optional]

The name of the event object. The name is limited to 
      <b>MAX_PATH</b> characters. Name comparison is case sensitive.

If <i>lpName</i> is <b>NULL</b>, the event object is created without a name.

If <i>lpName</i> matches the name of another kind of object in the same namespace (such as an existing semaphore, mutex, waitable timer, job, or 
       file-mapping object), the function fails and the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns 
       <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session 
        namespace. The remainder of the name can contain any character except the backslash character (\\). For more 
        information, see <a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined 
        for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

### -param dwFlags [in]

This parameter can be 0 or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_EVENT_INITIAL_SET"></a><a id="create_event_initial_set"></a><dl>
<dt><b>CREATE_EVENT_INITIAL_SET</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The initial state of the event object is signaled; otherwise, it is nonsignaled.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_EVENT_MANUAL_RESET"></a><a id="create_event_manual_reset"></a><dl>
<dt><b>CREATE_EVENT_MANUAL_RESET</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The event must be manually reset using the <a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a> function. Any number of 
    waiting threads, or threads that subsequently begin wait operations for the specified event object, can be 
    released while the object's state is signaled.

If this flag is not specified, the system automatically resets the event after releasing a single waiting thread.

</td>
</tr>
</table>

### -param dwDesiredAccess [in]

The access mask for the event object. For a list of access rights, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is a handle to the event object. If the named event object existed 
       before the function call, the function returns a handle to the existing object and 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
       <b>ERROR_ALREADY_EXISTS</b>.
     

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Any thread of the calling process can specify the event-object handle in a call to one of the 
    <a href="/windows/desktop/Sync/wait-functions">wait functions</a>. The single-object wait functions return 
    when the state of the specified object is signaled. The multiple-object wait functions can be instructed to 
    return either when any one or when all of the specified objects are signaled. When a wait function returns, the 
    waiting thread is released to continue its execution.
   

The initial state of the event object is specified by the <i>dwFlags</i> parameter. Use 
    the <a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a> function to set the state of an event object to 
    signaled. Use the <a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a> function to reset 
    the state of an event object to nonsignaled.
   

When the state of a manual-reset event object is signaled, it remains signaled until it is explicitly reset to 
    nonsignaled by the <a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a> function. Any number of 
    waiting threads, or threads that subsequently begin wait operations for the specified event object, can be 
    released while the object's state is signaled.
   

Multiple processes can have handles of the same event object, enabling use of the object for interprocess 
    synchronization. The following object-sharing mechanisms are available:
   

<ul>
<li>A child process created by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function 
      can inherit a handle to an event object if the <i>lpEventAttributes</i> parameter of 
      <b>CreateEvent</b> enabled inheritance.
     </li>
<li>A process can specify the event-object handle in a call to the 
      <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function to create a duplicate 
      handle that can be used by another process.
     </li>
<li>A process can specify the name of an event object in a call to the 
      <a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a> or <b>CreateEvent</b> function.
     </li>
</ul>
Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The 
    system closes the handle automatically when the process terminates. The event object is destroyed when its last 
    handle has been closed.
   





> [!NOTE]
> The synchapi.h header defines CreateEventEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/Sync/event-objects">Event Objects</a>



<a href="/windows/desktop/Sync/object-names">Object Names</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
