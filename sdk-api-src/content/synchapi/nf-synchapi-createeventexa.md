---
UID: NF:synchapi.CreateEventExA
title: CreateEventExA function
author: windows-sdk-content
description: Creates or opens a named or unnamed event object and returns a handle to the object.
old-location: base\createeventex.htm
old-project: sync
ms.assetid: 402a721d-8338-4df1-ba0b-074f868a1731
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: CREATE_EVENT_INITIAL_SET, CREATE_EVENT_MANUAL_RESET, CreateEventEx, CreateEventEx function, CreateEventExA, CreateEventExW, base.createeventex, synchapi/CreateEventEx, synchapi/CreateEventExA, synchapi/CreateEventExW, winbase/CreateEventEx, winbase/CreateEventExA, winbase/CreateEventExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.redist: 
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
 - CreateEventEx
 - CreateEventExA
 - CreateEventExW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CreateEventExA function


## -description


Creates or opens a named or unnamed event object and returns a handle to the object.


## -parameters




### -param lpEventAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure. If 
      <i>lpEventAttributes</i> is <b>NULL</b>, the event handle cannot be inherited by child processes.

The <b>lpSecurityDescriptor</b> member of the structure specifies a 
       <a href="https://msdn.microsoft.com/4ab0e7b1-1b44-4368-b2bd-106c9d2c652c">security descriptor</a> for the new 
       event. If <i>lpEventAttributes</i> is <b>NULL</b>, the event gets a default security descriptor. 
       The ACLs in the default security descriptor for an event come from the primary or impersonation token of the creator.
     


### -param lpName [in, optional]

The name of the event object. The name is limited to 
      <b>MAX_PATH</b> characters. Name comparison is case sensitive.

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


### -param dwFlags [in]

This parameter can be one or more of the following values.

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
The event must be manually reset using the <a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a> function. Any number of 
    waiting threads, or threads that subsequently begin wait operations for the specified event object, can be 
    released while the object's state is signaled.

If this flag is not specified, the system automatically resets the event after releasing a single waiting thread.

</td>
</tr>
</table>
 


### -param dwDesiredAccess [in]

The access mask for the event object. For a list of access rights, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is a handle to the event object. If the named event object existed 
       before the function call, the function returns a handle to the existing object and 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
       <b>ERROR_ALREADY_EXISTS</b>.
     

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
     




## -remarks



Any thread of the calling process can specify the event-object handle in a call to one of the 
    <a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>. The single-object wait functions return 
    when the state of the specified object is signaled. The multiple-object wait functions can be instructed to 
    return either when any one or when all of the specified objects are signaled. When a wait function returns, the 
    waiting thread is released to continue its execution.
   

The initial state of the event object is specified by the <i>dwFlags</i> parameter. Use 
    the <a href="https://msdn.microsoft.com/b474eef1-5df9-4729-b940-0c5f201c5f31">SetEvent</a> function to set the state of an event object to 
    signaled. Use the <a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a> function to reset 
    the state of an event object to nonsignaled.
   

When the state of a manual-reset event object is signaled, it remains signaled until it is explicitly reset to 
    nonsignaled by the <a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a> function. Any number of 
    waiting threads, or threads that subsequently begin wait operations for the specified event object, can be 
    released while the object's state is signaled.
   

Multiple processes can have handles of the same event object, enabling use of the object for interprocess 
    synchronization. The following object-sharing mechanisms are available:
   

<ul>
<li>A child process created by the <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function 
      can inherit a handle to an event object if the <i>lpEventAttributes</i> parameter of 
      <b>CreateEvent</b> enabled inheritance.
     </li>
<li>A process can specify the event-object handle in a call to the 
      <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function to create a duplicate 
      handle that can be used by another process.
     </li>
<li>A process can specify the name of an event object in a call to the 
      <a href="https://msdn.microsoft.com/46741024-ace3-44d6-b8a6-5621ad121a1a">OpenEvent</a> or <b>CreateEvent</b> function.
     </li>
</ul>
Use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the handle. The 
    system closes the handle automatically when the process terminates. The event object is destroyed when its last 
    handle has been closed.
   




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/63dc2991-e070-4981-9e2d-90b4fdaaee7a">Event Objects</a>



<a href="https://msdn.microsoft.com/00a00227-45fc-49a1-8ff5-aeccb172d16a">Object Names</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

