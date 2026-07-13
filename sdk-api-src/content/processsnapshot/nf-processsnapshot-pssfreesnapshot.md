---
UID: NF:processsnapshot.PssFreeSnapshot
title: PssFreeSnapshot function (processsnapshot.h)
description: Frees a snapshot.
helpviewer_keywords: ["PssFreeSnapshot","PssFreeSnapshot function","proc_snap.pssfreesnapshot","processsnapshot/PssFreeSnapshot"]
old-location: proc_snap\pssfreesnapshot.htm
tech.root: proc_snap
ms.assetid: 5D062AE6-2F7C-4121-AB6E-9BFA06AB36C6
ms.date: 12/05/2018
ms.keywords: PssFreeSnapshot, PssFreeSnapshot function, proc_snap.pssfreesnapshot, processsnapshot/PssFreeSnapshot
req.header: processsnapshot.h
req.include-header: 
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
req.lib: kernel32.Lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PssFreeSnapshot
 - processsnapshot/PssFreeSnapshot
dev_langs:
 - c++
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
---

# PssFreeSnapshot function


## -description

Frees a snapshot.

## -parameters

### -param ProcessHandle [in]

A handle to the process that contains the snapshot. The handle must have <b>PROCESS_VM_READ</b>, <b>PROCESS_VM_OPERATION</b>, and <b>PROCESS_DUP_HANDLE</b> rights. If the snapshot was captured from the current process, or duplicated into the current process, then pass in the result of <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a>.

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
 

All error codes are defined in winerror.h. Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.

## -remarks

This API can free snapshot handles in the context of either the local or remote processes. If the snapshot was captured in the local process with <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psscapturesnapshot">PssCaptureSnapshot</a>, or duplicated into the local process with <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-pssduplicatesnapshot">PssDuplicateSnapshot</a>, then specify the result of <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> as the process handle. If the snapshot is in the context of a remote process (for example, duplicated into the remote process), then specify the handle to that process.

The operation does not protect against concurrent access to the same descriptor.

For remote process frees, only snapshot handles that were created with<b> PSS_CREATE_USE_VM_ALLOCATIONS</b> or duplicated remotely can be freed by this API.

The behavior of this routine on a descriptor that has already been freed is undefined.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>