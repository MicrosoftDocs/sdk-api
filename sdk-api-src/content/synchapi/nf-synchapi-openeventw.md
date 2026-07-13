---
UID: NF:synchapi.OpenEventW
title: OpenEventW function (synchapi.h)
description: Opens an existing named event object. (Unicode)
helpviewer_keywords: ["OpenEvent", "OpenEvent function", "OpenEventW", "_win32_openevent", "base.openevent", "synchapi/OpenEvent", "synchapi/OpenEventW"]
old-location: base\openevent.htm
tech.root: base
ms.assetid: 46741024-ace3-44d6-b8a6-5621ad121a1a
ms.date: 12/05/2018
ms.keywords: OpenEvent, OpenEvent function, OpenEventA, OpenEventW, _win32_openevent, base.openevent, synchapi/OpenEvent, synchapi/OpenEventA, synchapi/OpenEventW, winbase/OpenEvent, winbase/OpenEventA, winbase/OpenEventW
req.header: synchapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenEventW (Unicode) and OpenEventA (ANSI)
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
 - OpenEventW
 - synchapi/OpenEventW
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
 - OpenEvent
 - OpenEventA
 - OpenEventW
---

# OpenEventW function


## -description

Opens an existing named event object.

## -parameters

### -param dwDesiredAccess [in]

The access to the event object. The function fails if the security descriptor of the specified object does not permit the requested access for the calling process. For a list of access rights, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

### -param bInheritHandle [in]

If this value is <b>TRUE</b>, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.

### -param lpName [in]

The  name of the event to be opened. Name comparisons are case sensitive.

This function can open objects in a private namespace. For more information, see <a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

<b>Terminal Services:  </b>The name can have a "Global\" or "Local\" prefix to explicitly open an object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\\). For more information, see 
<a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>.

<b>Note</b>  Fast user switching is implemented using Terminal Services sessions. The first user to log on uses session 0, the next user to log on uses session 1, and so on. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

## -returns

If the function succeeds, the return value is a handle to the event object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>OpenEvent</b> function enables multiple processes to open handles of the same event object. The function succeeds only if some process has already created the event by using the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function. The calling process can use the returned handle in any function that requires a handle to an event object, subject to the limitations of the access specified in the <i>dwDesiredAccess</i> parameter.

The handle can be duplicated by using the <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function. Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The system closes the handle automatically when the process terminates. The event object is destroyed when its last handle has been closed.





> [!NOTE]
> The synchapi.h header defines OpenEvent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="/windows/desktop/Sync/event-objects">Event Objects</a>



<a href="/windows/desktop/Sync/object-names">Object Names</a>



<a href="/windows/desktop/api/winbase/nf-winbase-pulseevent">PulseEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
