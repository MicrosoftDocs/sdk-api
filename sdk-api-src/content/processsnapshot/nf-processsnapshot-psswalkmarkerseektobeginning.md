---
UID: NF:processsnapshot.PssWalkMarkerSeekToBeginning
title: PssWalkMarkerSeekToBeginning function (processsnapshot.h)
description: Rewinds a walk marker back to the beginning.
helpviewer_keywords: ["PssWalkMarkerSeekToBeginning","PssWalkMarkerSeekToBeginning function","proc_snap.psswalkmarkerseektobeginning","processsnapshot/PssWalkMarkerSeekToBeginning"]
old-location: proc_snap\psswalkmarkerseektobeginning.htm
tech.root: proc_snap
ms.assetid: BE0FA122-3966-4827-9DA3-A98A162EF270
ms.date: 12/05/2018
ms.keywords: PssWalkMarkerSeekToBeginning, PssWalkMarkerSeekToBeginning function, proc_snap.psswalkmarkerseektobeginning, processsnapshot/PssWalkMarkerSeekToBeginning
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
 - PssWalkMarkerSeekToBeginning
 - processsnapshot/PssWalkMarkerSeekToBeginning
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
 - PssWalkMarkerSeekToBeginning
---

# PssWalkMarkerSeekToBeginning function


## -description

Rewinds a walk marker back to the beginning.

## -parameters

### -param WalkMarkerHandle [in]

A handle to the walk marker.

## -returns

This function returns <b>ERROR_SUCCESS</b> on success.

All error codes are defined in winerror.h. Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>