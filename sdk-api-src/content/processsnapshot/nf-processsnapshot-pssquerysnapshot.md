---
UID: NF:processsnapshot.PssQuerySnapshot
title: PssQuerySnapshot function (processsnapshot.h)
description: Queries the snapshot.
helpviewer_keywords: ["PssQuerySnapshot","PssQuerySnapshot function","proc_snap.pssquerysnapshot","processsnapshot/PssQuerySnapshot"]
old-location: proc_snap\pssquerysnapshot.htm
tech.root: proc_snap
ms.assetid: D9580147-28ED-4FF5-B7DB-844ACB19769F
ms.date: 12/05/2018
ms.keywords: PssQuerySnapshot, PssQuerySnapshot function, proc_snap.pssquerysnapshot, processsnapshot/PssQuerySnapshot
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
 - PssQuerySnapshot
 - processsnapshot/PssQuerySnapshot
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
 - PssQuerySnapshot
---

# PssQuerySnapshot function


## -description

Queries the snapshot.

## -parameters

### -param SnapshotHandle [in]

A handle to the snapshot to query.

### -param InformationClass [in]

An enumerator member that selects what information to query. For more information, see <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_query_information_class">PSS_QUERY_INFORMATION_CLASS</a>.

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
 

All error codes are defined in winerror.h. Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>