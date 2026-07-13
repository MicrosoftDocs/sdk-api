---
UID: NF:processsnapshot.PssWalkSnapshot
title: PssWalkSnapshot function (processsnapshot.h)
description: Returns information from the current walk position and advanced the walk marker to the next position.
helpviewer_keywords: ["PssWalkSnapshot","PssWalkSnapshot function","proc_snap.psswalksnapshot","processsnapshot/PssWalkSnapshot"]
old-location: proc_snap\psswalksnapshot.htm
tech.root: proc_snap
ms.assetid: C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0
ms.date: 12/05/2018
ms.keywords: PssWalkSnapshot, PssWalkSnapshot function, proc_snap.psswalksnapshot, processsnapshot/PssWalkSnapshot
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
 - PssWalkSnapshot
 - processsnapshot/PssWalkSnapshot
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
 - PssWalkSnapshot
---

# PssWalkSnapshot function


## -description

Returns information from the current walk position and advances the walk marker to the next position.

## -parameters

### -param SnapshotHandle [in]

A handle to the snapshot.

### -param InformationClass [in]

The type of information to return. For more information, see <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_walk_information_class">PSS_WALK_INFORMATION_CLASS</a>.

### -param WalkMarkerHandle [in]

A handle to a walk marker. The walk marker indicates the walk position from which data is to be returned. <b>PssWalkSnapshot</b> advances the walk marker to the next walk position in time order before returning to the caller.

### -param Buffer [out]

The snapshot information that this function returns.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
<i>Buffer</i> is <b>NULL</b>, and there is data at the current position to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The walk has completed and there are no more items to return.

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

## -remarks

For snapshot data types that have a variable number of instances within a snapshot, you use the <b>PssWalkSnapshot</b> function to obtain the instances one after another. You set the <i>InformationClass</i> parameter to specify the type of data.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>
