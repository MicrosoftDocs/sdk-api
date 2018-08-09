---
UID: NF:synchapi.CreateEventW
title: CreateEventW function
author: windows-sdk-content
description: Creates or opens a named or unnamed event object.
old-location: base\createevent.htm
old-project: sync
ms.assetid: 1f6d946e-c74c-4599-ac3d-b709216a0900
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateEvent, CreateEvent function, CreateEventA, CreateEventW, _win32_createevent, base.createevent, synchapi/CreateEvent, synchapi/CreateEventA, synchapi/CreateEventW, winbase/CreateEvent, winbase/CreateEventA, winbase/CreateEventW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
tech.root: 
req.typenames: ITEMPROP, *LPITEMPROP
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CreateEventW function


## -description


Creates or opens a named or unnamed event object.

To specify an access mask for the object, use the <a href="https://msdn.microsoft.com/402a721d-8338-4df1-ba0b-074f868a1731">CreateEventEx</a> function.


## -parameters




### -param lpEventAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure. If 
      this parameter is <b>NULL</b>, the handle cannot be inherited by child processes. 
      

The <b>lpSecurityDescriptor</b> member of the structure specifies a 
       <a href="https://msdn.microsoft.com/4ab0e7b1-1b44-4368-b2bd-106c9d2c652c">security descriptor</a> for the new 
       event. If <i>lpEventAttributes</i> is <b>NULL</b>, the event gets a default security descriptor. 
       The ACLs in the default security descriptor for an event come from the primary or impersonation token of the creator.


### -param bManualReset [in]

If this parameter is <b>TRUE</b>, the function creates a manual-reset event object, which requires the use of the 
      <a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a> function to set the event state to nonsignaled. If 
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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns 
       <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session 
        namespace. The remainder of the name can contain any character except the backslash character (\). For more 
        information, see <a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined 
        for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.


## -returns



If the function succeeds, the return value is a handle to the event object. If the named event object existed 
       before the function call, the function returns a handle to the existing object and 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
       <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The handle returned by <b>CreateEvent</b> has the 
    <b>EVENT_ALL_ACCESS</b> access right; it can be used in any function that requires a handle to 
    an event object, provided that the caller has been granted access. If an event is created from a service or a thread that is impersonating a different user, you can either apply a security descriptor to the event when you create it, or change the default security descriptor for the creating process by changing its default DACL. For more information, see 
    <a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security 
    and Access Rights</a>.

Any thread of the calling process can specify the event-object handle in a call to one of the 
    <a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>. The single-object wait functions return 
    when the state of the specified object is signaled. The multiple-object wait functions can be instructed to 
    return either when any one or when all of the specified objects are signaled. When a wait function returns, the 
    waiting thread is released to continue its execution.

The initial state of the event object is specified by the <i>bInitialState</i> parameter. Use 
    the <a href="https://msdn.microsoft.com/b474eef1-5df9-4729-b940-0c5f201c5f31">SetEvent</a> function to set the state of an event object to 
    signaled. Use the <a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a> function to reset 
    the state of an event object to nonsignaled.

When the state of a manual-reset event object is signaled, it remains signaled until it is explicitly reset to 
    nonsignaled by the <a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a> function. Any number of 
    waiting threads, or threads that subsequently begin wait operations for the specified event object, can be 
    released while the object's state is signaled.

When the state of an auto-reset event object is signaled, it remains signaled until a single waiting thread is 
    released; the system then automatically resets the state to nonsignaled. If no threads are waiting, the event 
    object's state remains signaled.

Multiple processes can have handles of the same event object, enabling use of the object for interprocess 
    synchronization. The following object-sharing mechanisms are available:

<ul>
<li>A child process created by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> function 
      can inherit a handle to an event object if the <i>lpEventAttributes</i> parameter of 
      <b>CreateEvent</b> enabled inheritance.</li>
<li>A process can specify the event-object handle in a call to the 
      <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function to create a duplicate 
      handle that can be used by another process.</li>
<li>A process can specify the name of an event object in a call to the 
      <a href="https://msdn.microsoft.com/46741024-ace3-44d6-b8a6-5621ad121a1a">OpenEvent</a> or <b>CreateEvent</b> function.</li>
</ul>
Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle. The 
    system closes the handle automatically when the process terminates. The event object is destroyed when its last 
    handle has been closed.


#### Examples

For an example that uses <b>CreateEvent</b>, see 
     <a href="https://msdn.microsoft.com/f3f455bb-7563-4920-a728-f75fa5854dc9">Using Event Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/402a721d-8338-4df1-ba0b-074f868a1731">CreateEventEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544323">Event Objects</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557762">Object Names</a>



<a href="https://msdn.microsoft.com/46741024-ace3-44d6-b8a6-5621ad121a1a">OpenEvent</a>



<a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/b474eef1-5df9-4729-b940-0c5f201c5f31">SetEvent</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

