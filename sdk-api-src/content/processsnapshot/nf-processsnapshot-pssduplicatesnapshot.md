---
UID: NF:processsnapshot.PssDuplicateSnapshot
title: PssDuplicateSnapshot function
author: windows-sdk-content
description: Duplicates a snapshot handle from one process to another.
old-location: proc_snap\pssduplicatesnapshot.htm
tech.root: proc_snap
ms.assetid: 5D2751F3-E7E1-4917-8060-E2BC8A7A3DEA
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PssDuplicateSnapshot, PssDuplicateSnapshot function, proc_snap.pssduplicatesnapshot, processsnapshot/PssDuplicateSnapshot
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: 
req.dll: Kernel32.dll
req.irql: 
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
 - PssDuplicateSnapshot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PssDuplicateSnapshot function


## -description


Duplicates a snapshot handle from one process to another.


## -parameters




### -param SourceProcessHandle [in]

A handle to the source process from which the original snapshot was captured. The handle must have <b>PROCESS_VM_READ</b> and <b>PROCESS_DUP_HANDLE</b> rights.


### -param SnapshotHandle [in]

A handle to the snapshot to duplicate. This handle must be in the context of the source process.


### -param TargetProcessHandle [in]

A handle to the target process that receives the duplicate snapshot. The handle must have <b>PROCESS_VM_OPERATION</b>, <b>PROCESS_VM_WRITE</b>, and <b>PROCESS_DUP_HANDLE</b> rights.


### -param TargetSnapshotHandle [out]

A handle to the duplicate snapshot that this function creates, in the context of the target process.


### -param Flags [in, optional]

The duplication flags. For more information, see <a href="https://msdn.microsoft.com/CAD06441-750F-42FC-A95A-7CAA79F31348">PSS_DUPLICATE_FLAGS</a>.


## -returns



This function returns <b>ERROR_SUCCESS</b> on success or the following error code.

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
</table>
 

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

