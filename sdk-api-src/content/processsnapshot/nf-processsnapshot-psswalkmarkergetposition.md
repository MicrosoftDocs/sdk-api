---
UID: NF:processsnapshot.PssWalkMarkerGetPosition
title: PssWalkMarkerGetPosition function (processsnapshot.h)
description: Returns the current position of a walk marker.
helpviewer_keywords: ["PssWalkMarkerGetPosition","PssWalkMarkerGetPosition function","proc_snap.psswalkmarkergetposition","processsnapshot/PssWalkMarkerGetPosition"]
old-location: proc_snap\psswalkmarkergetposition.htm
tech.root: proc_snap
ms.assetid: A2058E81-2B01-4436-ACC6-2A3E58BC4E27
ms.date: 12/05/2018
ms.keywords: PssWalkMarkerGetPosition, PssWalkMarkerGetPosition function, proc_snap.psswalkmarkergetposition, processsnapshot/PssWalkMarkerGetPosition
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
 - PssWalkMarkerGetPosition
 - processsnapshot/PssWalkMarkerGetPosition
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
 - PssWalkMarkerGetPosition
---

# PssWalkMarkerGetPosition function


## -description

Returns the current position of a walk marker.

## -parameters

### -param WalkMarkerHandle [in]

A  handle to the walk marker.

### -param Position [out]

The walk marker position that this function returns.

## -returns

This function returns <b>ERROR_SUCCESS</b> on success.

All error codes are defined in winerror.h. Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.

## -remarks

The position value compared to the values of other positions is not of any significance. The only valid use of the position is to set the current position using the <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalkmarkersetposition">PssWalkMarkerSetPosition</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>