---
UID: NF:processsnapshot.PssWalkMarkerFree
title: PssWalkMarkerFree function (processsnapshot.h)
description: Frees a walk marker created by PssWalkMarkerCreate.
helpviewer_keywords: ["PssWalkMarkerFree","PssWalkMarkerFree function","proc_snap.psswalkmarkerfree","processsnapshot/PssWalkMarkerFree"]
old-location: proc_snap\psswalkmarkerfree.htm
tech.root: proc_snap
ms.assetid: 74158846-6A5F-4F81-B4D7-46DED1EE017C
ms.date: 12/05/2018
ms.keywords: PssWalkMarkerFree, PssWalkMarkerFree function, proc_snap.psswalkmarkerfree, processsnapshot/PssWalkMarkerFree
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
 - PssWalkMarkerFree
 - processsnapshot/PssWalkMarkerFree
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
 - PssWalkMarkerFree
---

# PssWalkMarkerFree function


## -description

Frees a walk marker created by <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalkmarkercreate">PssWalkMarkerCreate</a>.

## -parameters

### -param WalkMarkerHandle [in]

A handle to the walk marker.

## -returns

This function returns <b>ERROR_SUCCESS</b> on success.

All error codes are defined in winerror.h. Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.

## -remarks

If <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalkmarkercreate">PssWalkMarkerCreate</a> used <b>AllocRoutine</b> of a custom allocator to create the walk marker, <b>PssWalkMarkerFree</b> uses the <b>FreeRoutine</b> of the allocator.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>