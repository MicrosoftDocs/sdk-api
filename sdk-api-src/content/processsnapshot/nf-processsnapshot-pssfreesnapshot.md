---
UID: NF:processsnapshot.PssFreeSnapshot
title: PssFreeSnapshot function
author: windows-sdk-content
description: Frees a snapshot.
old-location: proc_snap\pssfreesnapshot.htm
old-project: proc_snap
ms.assetid: 5D062AE6-2F7C-4121-AB6E-9BFA06AB36C6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: PssFreeSnapshot, PssFreeSnapshot function, proc_snap.pssfreesnapshot, processsnapshot/PssFreeSnapshot
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processsnapshot.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PSS_WALK_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Processsnapshot-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PssFreeSnapshot
product: Windows
targetos: Windows
req.lib: 
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# PssFreeSnapshot function


## -description


Frees a snapshot.


## -parameters




### -param ProcessHandle [in]

A handle to the process that contains the snapshot. The handle must have <b>PROCESS_VM_READ</b>, <b>PROCESS_VM_OPERATION</b>, and <b>PROCESS_DUP_HANDLE</b> rights. If the snapshot was captured from the current process, or duplicated into the current process, then pass in the result of <a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a>.


### -param SnapshotHandle [in]

A handle to the snapshot to free.


## -returns



This function returns <b>ERROR_SUCCESS</b> on success or one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The remote snapshot was not created with <b>PSS_CREATE_USE_VM_ALLOCATIONS</b>.

</td>
</tr>
</table>
 

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.




## -remarks



This API can free snapshot handles in the context of either the local or remote processes. If the snapshot was captured in the local process with <a href="https://msdn.microsoft.com/44F2CB48-A9F6-4131-B21C-9F27A27CECD5">PssCaptureSnapshot</a>, or duplicated into the local process with <a href="https://msdn.microsoft.com/5D2751F3-E7E1-4917-8060-E2BC8A7A3DEA">PssDuplicateSnapshot</a>, then specify the result of <a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a> as the process handle. If the snapshot is in the context of a remote process (for example, duplicated into the remote process), then specify the handle to that process.

The operation does not protect against concurrent access to the same descriptor.

For remote process frees, only snapshot handles that were created with<b> PSS_CREATE_USE_VM_ALLOCATIONS</b> or duplicated remotely can be freed by this API.

The behavior of this routine on a descriptor that has already been freed is undefined.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

