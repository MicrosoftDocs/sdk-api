---
UID: NF:processsnapshot.PssWalkMarkerCreate
title: PssWalkMarkerCreate function (processsnapshot.h)
description: Creates a walk marker.
helpviewer_keywords: ["PssWalkMarkerCreate","PssWalkMarkerCreate function","proc_snap.psswalkmarkercreate","processsnapshot/PssWalkMarkerCreate"]
old-location: proc_snap\psswalkmarkercreate.htm
tech.root: proc_snap
ms.assetid: 58E2FBAF-661C-45BE-A25A-A096AF52ED3E
ms.date: 12/05/2018
ms.keywords: PssWalkMarkerCreate, PssWalkMarkerCreate function, proc_snap.psswalkmarkercreate, processsnapshot/PssWalkMarkerCreate
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
 - PssWalkMarkerCreate
 - processsnapshot/PssWalkMarkerCreate
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
 - PssWalkMarkerCreate
---

# PssWalkMarkerCreate function


## -description

Creates a walk marker.

## -parameters

### -param Allocator [in, optional]

A structure that provides functions to allocate and free memory.  If you provide the structure, <b>PssWalkMarkerCreate</b> uses the functions to  allocate the internal walk marker structures. Otherwise it uses the default process heap. For more information, see <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_allocator">PSS_ALLOCATOR</a>.

### -param WalkMarkerHandle [out]

A handle to the walk marker that this function creates.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not allocate memory for the walk marker.

</td>
</tr>
</table>
 

All error codes are defined in winerror.h. Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.

## -remarks

The walk marker maintains the state of a walk, and can be used to reposition or rewind the walk.

The <i>Allocator</i> structure that provides the custom functions should remain valid for the lifetime of the walk marker. The custom functions are called from <b>PssWalkMarkerCreate</b>, <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalkmarkerfree">PssWalkMarkerFree</a> and <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a> using the same thread that calls <b>PssWalkMarkerCreate</b>, <b>PssWalkMarkerFree</b> and <b>PssWalkSnapshot</b>. Therefore the custom functions need not be multi-threaded.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>