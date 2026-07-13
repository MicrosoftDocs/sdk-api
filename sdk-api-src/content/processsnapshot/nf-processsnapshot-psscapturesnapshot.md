---
UID: NF:processsnapshot.PssCaptureSnapshot
title: PssCaptureSnapshot function (processsnapshot.h)
description: Captures a snapshot of a target process.
helpviewer_keywords: ["PssCaptureSnapshot","PssCaptureSnapshot function","proc_snap.psscapturesnapshot","processsnapshot/PssCaptureSnapshot"]
old-location: proc_snap\psscapturesnapshot.htm
tech.root: proc_snap
ms.assetid: 44F2CB48-A9F6-4131-B21C-9F27A27CECD5
ms.date: 12/05/2018
ms.keywords: PssCaptureSnapshot, PssCaptureSnapshot function, proc_snap.psscapturesnapshot, processsnapshot/PssCaptureSnapshot
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
 - PssCaptureSnapshot
 - processsnapshot/PssCaptureSnapshot
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
 - PssCaptureSnapshot
---

# PssCaptureSnapshot function


## -description

Captures a snapshot of a target process.

## -parameters

### -param ProcessHandle [in]

A handle to the target process.

### -param CaptureFlags [in]

Flags that specify what to capture. For more information, see <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_capture_flags">PSS_CAPTURE_FLAGS</a>.

### -param ThreadContextFlags [in, optional]

The <b>CONTEXT</b> record flags to capture if <i>CaptureFlags</i> specifies thread contexts.

### -param SnapshotHandle [out]

A handle to the snapshot that this function captures.

## -returns

This function returns <b>ERROR_SUCCESS</b> on success.

All error codes are defined in winerror.h. Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.