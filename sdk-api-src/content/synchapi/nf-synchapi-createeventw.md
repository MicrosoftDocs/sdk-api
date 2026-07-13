---
UID: NF:synchapi.CreateEventW
title: CreateEventW function (synchapi.h)
description: Creates or opens a named or unnamed event object. (Unicode)
helpviewer_keywords: ["CreateEvent", "CreateEvent function", "CreateEventW", "_win32_createevent", "base.createevent", "synchapi/CreateEvent", "synchapi/CreateEventW"]
old-location: base\createevent.htm
tech.root: base
ms.assetid: 1f6d946e-c74c-4599-ac3d-b709216a0900
ms.date: 12/05/2018
ms.keywords: CreateEvent, CreateEvent function, CreateEventA, CreateEventW, _win32_createevent, base.createevent, synchapi/CreateEvent, synchapi/CreateEventA, synchapi/CreateEventW, winbase/CreateEvent, winbase/CreateEventA, winbase/CreateEventW
req.header: synchapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateEventW (Unicode) and CreateEventA (ANSI)
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
 - CreateEventW
 - synchapi/CreateEventW
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
 - CreateEvent
 - CreateEventA
 - CreateEventW
---

# CreateEventW function


## -description

Creates or opens a named or unnamed event object.

To specify an access mask for the object, use the <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventexa">CreateEventEx</a> function.

## -parameters

### -param lpEventAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure. If 
      this parameter is <b>NULL</b>, the handle cannot be inherited by child processes. 
      

The <b>lpSecurityDescriptor</b> member of the structure specifies a 
       <a href="/windows/desktop/SecAuthZ/security-descriptors">security descriptor</a> for the new 
       event. If <i>lpEventAttributes</i> is <b>NULL</b>, the event gets a default security descriptor. 
       The ACLs in the default security descriptor for an event come from the primary or impersonation token of the creator.

### -param bManualReset [in]

If this parameter is <b>TRUE</b>, the function creates a manual-reset event object, which requires the use of the 
      <a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a> function to set the event state to nonsignaled. If 
      this parameter is <b>FALSE</b>, the function creates an auto-reset event object, and system automatically resets the 
      event state to nonsignaled after a single waiting thread has been released.

### -param bInitialState [in]

If this parameter is <b>TRUE</b>, the initial state of the event object is signaled; otherwise, it is nonsignaled.

### -param lpName [in, optional]

The name of the event object. The name is limited to 
      <b>MAX_PATH</b> characters. Name comparison is case sensitive. 
      

If <i>lpName</i> matches the name of an existing named event object, this function requests 
       the <b>EVENT_ALL_ACCESS</b> access right. In this case, the 
       <i>bManualReset</i> and <i>bInitialState</i> parameters are ignored 
       because they have already been set by the creating process. If the 
       <i>lpEventAttributes</i> parameter is not <b>NULL</b>, it determines whether the handle can be 
       inherited, but its security-descriptor member is ignored.

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

## -returns

If the function succeeds, the return value is a handle to the event object. If the named event object existed 
       before the function call, the function returns a handle to the existing object and 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
       <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The handle returned by <b>CreateEvent</b> has the 
    <b>EVENT_ALL_ACCESS</b> access right; it can be used in any function that requires a handle to 
    an event object, provided that the caller has been granted access. If an event is created from a service or a thread that is impersonating a different user, you can either apply a security descriptor to the event when you create it, or change the default security descriptor for the creating process by changing its default DACL. For more information, see 
    <a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security 
    and Access Rights</a>.

Any thread of the calling process can specify the event-object handle in a call to one of the 
    <a href="/windows/desktop/Sync/wait-functions">wait functions</a>. The single-object wait functions return 
    when the state of the specified object is signaled. The multiple-object wait functions can be instructed to 
    return either when any one or when all of the specified objects are signaled. When a wait function returns, the 
    waiting thread is released to continue its execution.

The initial state of the event object is specified by the <i>bInitialState</i> parameter. Use 
    the <a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a> function to set the state of an event object to 
    signaled. Use the <a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a> function to reset 
    the state of an event object to nonsignaled.

When the state of a manual-reset event object is signaled, it remains signaled until it is explicitly reset to 
    nonsignaled by the <a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a> function. Any number of 
    waiting threads, or threads that subsequently begin wait operations for the specified event object, can be 
    released while the object's state is signaled.

When the state of an auto-reset event object is signaled, it remains signaled until a single waiting thread is 
    released; the system then automatically resets the state to nonsignaled. If no threads are waiting, the event 
    object's state remains signaled.

Multiple processes can have handles of the same event object, enabling use of the object for interprocess 
    synchronization. The following object-sharing mechanisms are available:

<ul>
<li>A child process created by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function 
      can inherit a handle to an event object if the <i>lpEventAttributes</i> parameter of 
      <b>CreateEvent</b> enabled inheritance.</li>
<li>A process can specify the event-object handle in a call to the 
      <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function to create a duplicate 
      handle that can be used by another process.</li>
<li>A process can specify the name of an event object in a call to the 
      <a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a> or <b>CreateEvent</b> function.</li>
</ul>
Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The 
    system closes the handle automatically when the process terminates. The event object is destroyed when its last 
    handle has been closed.


#### Examples

For an example that uses <b>CreateEvent</b>, see 
     <a href="/windows/desktop/Sync/using-event-objects">Using Event Objects</a>.

<div class="code"></div>




> [!NOTE]
> The synchapi.h header defines CreateEvent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventexa">CreateEventEx</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="/windows/desktop/Sync/event-objects">Event Objects</a>



<a href="/windows/desktop/Sync/object-names">Object Names</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
