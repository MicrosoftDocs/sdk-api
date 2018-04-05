---
UID: NF:processsnapshot.PssCaptureSnapshot
title: PssCaptureSnapshot function
author: windows-driver-content
description: Captures a snapshot of a target process.
old-location: proc_snap\psscapturesnapshot.htm
old-project: proc_snap
ms.assetid: 44F2CB48-A9F6-4131-B21C-9F27A27CECD5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PssCaptureSnapshot, PssCaptureSnapshot function, proc_snap.psscapturesnapshot, processsnapshot/PssCaptureSnapshot
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
-	PssCaptureSnapshot
product: Windows
targetos: Windows
req.lib: 
req.dll: Kernel32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PssCaptureSnapshot function


## -description


Captures a snapshot of a target process.


## -parameters




### -param ProcessHandle [in]

A handle to the target process.


### -param CaptureFlags [in]

Flags that specify what to capture. For more information, see <a href="https://msdn.microsoft.com/6146DDA2-2475-45F8-86F3-65791B10743D">PSS_CAPTURE_FLAGS</a>.


### -param ThreadContextFlags [in, optional]

The <b>CONTEXT</b> record flags to capture if <i>CaptureFlags</i> specifies thread contexts.


### -param SnapshotHandle [out]

A handle to the snapshot that this function captures.


## -returns



This function returns <b>ERROR_SUCCESS</b> on success.

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.



