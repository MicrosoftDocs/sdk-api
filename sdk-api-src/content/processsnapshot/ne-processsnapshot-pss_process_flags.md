---
UID: NE:processsnapshot.__unnamed_enum_6
title: PSS_PROCESS_FLAGS (processsnapshot.h)
description: Flags that describe a process.
helpviewer_keywords: ["PSS_PROCESS_FLAGS","PSS_PROCESS_FLAGS enumeration","PSS_PROCESS_FLAGS_FROZEN","PSS_PROCESS_FLAGS_NONE","PSS_PROCESS_FLAGS_PROTECTED","PSS_PROCESS_FLAGS_RESERVED_03","PSS_PROCESS_FLAGS_RESERVED_04","PSS_PROCESS_FLAGS_WOW64","proc_snap.pss_process_flags","processsnapshot/PSS_PROCESS_FLAGS","processsnapshot/PSS_PROCESS_FLAGS_FROZEN","processsnapshot/PSS_PROCESS_FLAGS_NONE","processsnapshot/PSS_PROCESS_FLAGS_PROTECTED","processsnapshot/PSS_PROCESS_FLAGS_RESERVED_03","processsnapshot/PSS_PROCESS_FLAGS_RESERVED_04","processsnapshot/PSS_PROCESS_FLAGS_WOW64"]
old-location: proc_snap\pss_process_flags.htm
tech.root: proc_snap
ms.assetid: A1C793DD-EE93-47B6-8EA8-3A45DAD55F2D
ms.date: 12/05/2018
ms.keywords: PSS_PROCESS_FLAGS, PSS_PROCESS_FLAGS enumeration, PSS_PROCESS_FLAGS_FROZEN, PSS_PROCESS_FLAGS_NONE, PSS_PROCESS_FLAGS_PROTECTED, PSS_PROCESS_FLAGS_RESERVED_03, PSS_PROCESS_FLAGS_RESERVED_04, PSS_PROCESS_FLAGS_WOW64, proc_snap.pss_process_flags, processsnapshot/PSS_PROCESS_FLAGS, processsnapshot/PSS_PROCESS_FLAGS_FROZEN, processsnapshot/PSS_PROCESS_FLAGS_NONE, processsnapshot/PSS_PROCESS_FLAGS_PROTECTED, processsnapshot/PSS_PROCESS_FLAGS_RESERVED_03, processsnapshot/PSS_PROCESS_FLAGS_RESERVED_04, processsnapshot/PSS_PROCESS_FLAGS_WOW64
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
targetos: Windows
req.typenames: PSS_PROCESS_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_PROCESS_FLAGS
 - processsnapshot/PSS_PROCESS_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_PROCESS_FLAGS
---

# PSS_PROCESS_FLAGS enumeration


## -description

Flags that describe a process.

## -enum-fields

### -field PSS_PROCESS_FLAGS_NONE:0x00000000

No flag.

### -field PSS_PROCESS_FLAGS_PROTECTED:0x00000001

The process is protected.

### -field PSS_PROCESS_FLAGS_WOW64:0x00000002

The process is a 32-bit process running on a 64-bit native OS.

### -field PSS_PROCESS_FLAGS_RESERVED_03:0x00000004

Undefined.

### -field PSS_PROCESS_FLAGS_RESERVED_04:0x00000008

Undefined.

### -field PSS_PROCESS_FLAGS_FROZEN:0x00000010

The process is frozen; for example,  a debugger is attached and broken into the process or a Store process is suspended by a lifetime management service.

## -remarks

There are <b>PSS_PROCESS_FLAGS</b> members in the <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_process_information">PSS_PROCESS_INFORMATION</a> and <a href="/previous-versions/windows/desktop/api/processsnapshot/ns-processsnapshot-pss_handle_entry">PSS_HANDLE_ENTRY</a> structures.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>
