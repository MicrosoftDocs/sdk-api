---
UID: NF:memoryapi.CreateMemoryResourceNotification
title: CreateMemoryResourceNotification function (memoryapi.h)
description: Creates a memory resource notification object.
helpviewer_keywords: ["CreateMemoryResourceNotification","CreateMemoryResourceNotification function","HighMemoryResourceNotification","LowMemoryResourceNotification","_win32_creatememoryresourcenotification","base.creatememoryresourcenotification","winbase/CreateMemoryResourceNotification"]
old-location: base\creatememoryresourcenotification.htm
tech.root: base
ms.assetid: e4d794ca-4abb-4933-bd07-793e78c52881
ms.date: 12/05/2018
ms.keywords: CreateMemoryResourceNotification, CreateMemoryResourceNotification function, HighMemoryResourceNotification, LowMemoryResourceNotification, _win32_creatememoryresourcenotification, base.creatememoryresourcenotification, winbase/CreateMemoryResourceNotification
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
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
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateMemoryResourceNotification
 - memoryapi/CreateMemoryResourceNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - CreateMemoryResourceNotification
---

# CreateMemoryResourceNotification function


## -description

Creates a memory resource notification object.

## -parameters

### -param NotificationType [in]

The memory condition under which the object is to be signaled. This parameter can be one of the following 
      values from the <b>MEMORY_RESOURCE_NOTIFICATION_TYPE</b> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LowMemoryResourceNotification"></a><a id="lowmemoryresourcenotification"></a><a id="LOWMEMORYRESOURCENOTIFICATION"></a><dl>
<dt><b>LowMemoryResourceNotification</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Available physical memory is running low.

</td>
</tr>
<tr>
<td width="40%"><a id="HighMemoryResourceNotification"></a><a id="highmemoryresourcenotification"></a><a id="HIGHMEMORYRESOURCENOTIFICATION"></a><dl>
<dt><b>HighMemoryResourceNotification</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Available physical memory is high.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a handle to a memory resource notification object.

If the function fails, the return value is <b>NULL</b>. To get extended  information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Applications can use memory resource notification events to scale the memory usage as appropriate. If 
    available memory is low, the application can reduce its working set. If available memory is high, the application 
    can allocate more memory.

Any thread of the calling process can specify the memory resource notification handle in a call to the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-querymemoryresourcenotification">QueryMemoryResourceNotification</a> 
    function or one of the <a href="/windows/desktop/Sync/wait-functions">wait functions</a>. The state of the 
    object is signaled when the specified memory condition exists. This is a system-wide event, so all applications 
    receive notification when the object is signaled. Note that there is a range of memory availability where neither 
    the <b>LowMemoryResourceNotification</b> or 
    <b>HighMemoryResourceNotification</b> object is signaled. In this case, applications should 
    attempt to keep the memory use constant.

Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle. The 
    system closes the handle automatically when the process terminates. The memory resource notification object is 
    destroyed when its last handle has been closed.

To compile an application that uses this function, define the <b>_WIN32_WINNT</b> macro 
    as 0x0501 or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-querymemoryresourcenotification">QueryMemoryResourceNotification</a>