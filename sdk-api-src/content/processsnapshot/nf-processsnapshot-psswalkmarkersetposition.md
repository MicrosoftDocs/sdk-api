---
UID: NF:processsnapshot.PssWalkMarkerSetPosition
title: PssWalkMarkerSetPosition function (processsnapshot.h)
description: Sets the position of a walk marker.
helpviewer_keywords: ["PssWalkMarkerSetPosition","PssWalkMarkerSetPosition function","proc_snap.psswalkmarkersetposition","processsnapshot/PssWalkMarkerSetPosition"]
old-location: proc_snap\psswalkmarkersetposition.htm
tech.root: proc_snap
ms.assetid: D89EA4DB-D8C6-43D1-B292-D24F1EAB2E43
ms.date: 12/05/2018
ms.keywords: PssWalkMarkerSetPosition, PssWalkMarkerSetPosition function, proc_snap.psswalkmarkersetposition, processsnapshot/PssWalkMarkerSetPosition
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
 - PssWalkMarkerSetPosition
 - processsnapshot/PssWalkMarkerSetPosition
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
 - PssWalkMarkerSetPosition
---

# PssWalkMarkerSetPosition function


## -description

Sets the position of a walk marker.

## -parameters

### -param WalkMarkerHandle [in]

A handle to the walk marker.

### -param Position [in]

The position to set. This is a position that the  <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalkmarkergetposition">PssWalkMarkerGetPosition</a> function provided.

## -returns

This function returns <b>ERROR_SUCCESS</b> on success or one of the following error codes.

All error codes are defined in winerror.h. Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>