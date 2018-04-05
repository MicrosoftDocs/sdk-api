---
UID: NF:processsnapshot.PssQuerySnapshot
title: PssQuerySnapshot function
author: windows-driver-content
description: Queries the snapshot.
old-location: proc_snap\pssquerysnapshot.htm
old-project: proc_snap
ms.assetid: D9580147-28ED-4FF5-B7DB-844ACB19769F
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PssQuerySnapshot, PssQuerySnapshot function, proc_snap.pssquerysnapshot, processsnapshot/PssQuerySnapshot
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
req.typenames: PSS_WALK_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	kernel32.dll
-	API-MS-Win-Core-Processsnapshot-l1-1-0.dll
-	KernelBase.dll
api_name:
-	PssQuerySnapshot
product: Windows
targetos: Windows
req.lib: 
req.dll: Kernel32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PssQuerySnapshot function


## -description


Queries the snapshot.


## -parameters




### -param SnapshotHandle [in]

A handle to the snapshot to query.


### -param InformationClass [in]

An enumerator member that selects what information to query. For more information, see <a href="https://msdn.microsoft.com/1C3E5BF4-5AC9-4012-B29D-49C35C0AF90B">PSS_QUERY_INFORMATION_CLASS</a>.


### -param Buffer [out]

The information that this function provides.


### -param BufferLength [in]

The size of <i>Buffer</i>, in bytes.


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
<dt><b>ERROR_BAD_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
The specified buffer length is invalid.

</td>
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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified information class is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested information is not in the snapshot.

</td>
</tr>
</table>
 

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

