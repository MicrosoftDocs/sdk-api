---
UID: NE:processsnapshot.PSS_PROCESS_FLAGS
title: PSS_PROCESS_FLAGS
author: windows-sdk-content
description: Flags that describe a process.
old-location: proc_snap\pss_process_flags.htm
tech.root: proc_snap
ms.assetid: A1C793DD-EE93-47B6-8EA8-3A45DAD55F2D
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: PSS_PROCESS_FLAGS, PSS_PROCESS_FLAGS enumeration, PSS_PROCESS_FLAGS_FROZEN, PSS_PROCESS_FLAGS_NONE, PSS_PROCESS_FLAGS_PROTECTED, PSS_PROCESS_FLAGS_RESERVED_03, PSS_PROCESS_FLAGS_RESERVED_04, PSS_PROCESS_FLAGS_WOW64, proc_snap.pss_process_flags, processsnapshot/PSS_PROCESS_FLAGS, processsnapshot/PSS_PROCESS_FLAGS_FROZEN, processsnapshot/PSS_PROCESS_FLAGS_NONE, processsnapshot/PSS_PROCESS_FLAGS_PROTECTED, processsnapshot/PSS_PROCESS_FLAGS_RESERVED_03, processsnapshot/PSS_PROCESS_FLAGS_RESERVED_04, processsnapshot/PSS_PROCESS_FLAGS_WOW64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_PROCESS_FLAGS
product: Windows
targetos: Windows
req.typenames: PSS_PROCESS_FLAGS
req.redist: 
---

# PSS_PROCESS_FLAGS enumeration


## -description


Flags that describe a process.


## -enum-fields




### -field PSS_PROCESS_FLAGS_NONE

No flag.


### -field PSS_PROCESS_FLAGS_PROTECTED

The process is protected.


### -field PSS_PROCESS_FLAGS_WOW64

The process is a 32-bit process running on a 64-bit native OS.


### -field PSS_PROCESS_FLAGS_RESERVED_03

Undefined.


### -field PSS_PROCESS_FLAGS_RESERVED_04

Undefined.


### -field PSS_PROCESS_FLAGS_FROZEN

The process is frozen; for example,  a debugger is attached and broken into the process or a Store process is suspended by a lifetime management service.


## -remarks



There are <b>PSS_PROCESS_FLAGS</b> members in the <a href="https://msdn.microsoft.com/D629FA42-B501-4A0E-9B53-6D70E580B687">PSS_PROCESS_INFORMATION</a> and <a href="https://msdn.microsoft.com/F56E8C35-949A-4DEE-973F-CF24F6596036">PSS_HANDLE_ENTRY</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

